{\rtf1\ansi\ansicpg1252\cocoartf1561\cocoasubrtf400
{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 pipeline \{\
    agent any\
                    node \{\
                        def remote = [:]\
                        remote.host = '18.212.113.222'\
                        remote.user = 'root'\
                        remote.password = 'root'\
                        remote.allowAnyHosts = true\
                        stage('Remote SSH') \{\
                            sshCommand remote: remote, command: "docker build -t ziyanakthar/tomcat:latest$BUILD_NUMBER ."\
                            sshCommand remote: remote, command: "sudo docker login -u ziyanakthar -p Nasiranaaz"\
                        \}\
                    \}\
\}}