cmake_minimum_required(VERSION 3.0.2)

project(test)

install(
    DIRECTORY ispd2005 DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY ispd2015 DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY ispd2019 DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY dac2012 DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY iccad2014 DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY iccad2015.ot DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY ispd2005free DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

install(
    DIRECTORY mms DESTINATION thirdparty/DREAMPlace/${PROJECT_NAME}
    )

