#name of module created
set(kmodule_name "kedr_test_indicator_simulate_never")

add_test_indicator(${kmodule_name})

configure_file("${CMAKE_CURRENT_SOURCE_DIR}/test.sh.in"
	"${CMAKE_CURRENT_BINARY_DIR}/test.sh"
	@ONLY
)

kedr_test_add_script(fault_simulation_indicator_template.never.01
	"test.sh"
)
