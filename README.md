package org.firstinspires.ftc.teamcode;

import com.qualcomm.robotcore.eventloop.opmode.Autonomous;
import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;
import com.qualcomm.robotcore.hardware.DcMotor;
import com.qualcomm.robotcore.eventloop.opmode.TeleOp;

@Autonomous

public class CodersAuton extends LinearOpMode {

DcMotor frontLeft; 
DcMotor frontRight;
DcMotor backLeft;
DcMotor backRight;

@Override

   
public void runOpMode() {
   backLeft = hardwareMap.get (DcMotor.class,"backleft");
    backRight = hardwareMap.get (DcMotor.class,"backright");
   frontLeft= hardwareMap.get (DcMotor.class,"frontleft");
    frontRight= hardwareMap.get(DcMotor.class,"frontright");
    
frontLeft.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
frontRight.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
backLeft.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
backRight.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);

frontLeft.setDirection(DcMotor.Direction.REVERSE);
backLeft.setDirection(DcMotor.Direction.REVERSE);

waitForStart();
while(opModeIsActive()) {

//set target position (ticks that it moves)
frontLeft.setTargetPosition(5000);
frontRight.setTargetPosition(5000);
backLeft.setTargetPosition(5000);
backRight.setTargetPosition(5000);


//run to position

frontLeft.setMode(DcMotor.RunMode.RUN_TO_POSITION);
frontRight.setMode(DcMotor.RunMode.RUN_TO_POSITION);
backLeft.setMode(DcMotor.RunMode.RUN_TO_POSITION);
backRight.setMode(DcMotor.RunMode.RUN_TO_POSITION);

//set power
frontLeft.setPower(0.5);
frontRight.setPower(0.5);
backLeft.setPower(0.5);
backRight.setPower(0.5);


  


frontLeft.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
frontRight.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
backLeft.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
backRight.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);

/*frontLeft.setPower(0);
frontRight.setPower(0);
backLeft.setPower(0);
backRight.setPower(0);*/

}



       }
}


    // todo: write your code here


