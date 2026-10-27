# InOurEyes

**One image. One age. A new way to see learning.**

InOurEyes is an AI-powered visual curriculum lens. A teacher uploads one photograph, selects a child's age, and receives British curriculum outcomes that are genuinely supported by visible evidence in the image.

## MVP scope

- One photograph per analysis
- Ages 4–11
- British curriculum first
- Selected-age perspective only
- Visible evidence linked to curriculum outcomes
- No lesson plans or activity generation
- OpenAI API key remains server-side in AWS Secrets Manager

## Architecture

- Static frontend hosted with AWS Amplify
- Amazon Cognito authentication
- API Gateway HTTP API with JWT authorization
- AWS Lambda image-analysis backend
- OpenAI Responses API with vision and web search
- AWS Secrets Manager for the API key

## Deployment

The frontend configuration belongs in `config.js`. The AWS SAM backend is located in `backend/`.

Never commit an OpenAI API key to this repository.
