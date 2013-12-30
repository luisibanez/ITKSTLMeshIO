itk_module_test()

set(ITKIOSTLMeshTests
  itkSTLMeshIOTest.cxx
)

CreateTestDriver(ITKIOSTLMesh "${ITKIOSTLMesh-Test_LIBRARIES}" "${ITKIOSTLMeshTests}" )

itk_add_test(NAME itkSTLMeshIOTest00
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/sphere.vtk}
      ${ITK_TEST_OUTPUT_DIR}/sphere00.stl
)
