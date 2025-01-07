provider "aws" {
  region     = "us-west-1"
}
 
resource "aws_s3_bucket" "b1" {
  bucket = "vedveer-b1"
  acl    = "private"
 
  tags = {
    Name        = "Historical Logs"
    Environment = "Dev"
  }
 
  versioning {
    enabled = true
  }  
}