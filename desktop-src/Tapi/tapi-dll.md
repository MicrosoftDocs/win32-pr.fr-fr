---
description: Les dll TAPI, ainsi que le serveur TAPI (Tapisvr.exe), sont des abstractions cruciales qui séparent les applications de l’utilisateur final ou du serveur des fournisseurs de services. Une DLL TAPI conjointement avec le serveur TAPI fournit une interface cohérente entre ces deux couches.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff26274baf25047212a3f9f8e15c2211d90cbaa10db23674ae54dbb97bbfdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012202"
---
# <a name="tapi-dll"></a>DLL TAPI

Les dll TAPI, ainsi que le serveur TAPI (Tapisvr.exe), sont des abstractions cruciales qui séparent les applications de l’utilisateur final ou du serveur des fournisseurs de services. Une DLL TAPI conjointement avec le serveur TAPI fournit une interface cohérente entre ces deux couches.

Une application TAPI charge la DLL appropriée dans son espace de processus. Pendant l’initialisation, TAPI établit une liaison RPC avec Tapisvr.exe. Le serveur TAPI s’exécute dans le contexte de SVCHOST.

Il existe trois dll associées à l’interface TAPI : Tapi.dll, Tapi32.dll et Tapi3.dll. Ces dll se trouvent dans% SystemRoot% \\ system32. La figure suivante illustre les rôles de leurs rôles respectifs dans Microsoft Telephony :

![rôles des trois dll TAPI](images/dllserv.png)

Les applications 16 bits existantes sont liées à Tapi.dll. Tapi.dll est simplement une couche de thunk qui mappe les adresses 16 bits aux adresses 32 bits et transmet les demandes à Tapi32.dll.

Les applications TAPI 2. x 32 bits existantes sont liées à Tapi32.dll. Tapi32.dll est une couche de marshaling fine qui transfère les demandes de fonction vers le serveur TAPI (TAPISRV) et, si nécessaire, charge et appelle les dll du fournisseur de services multimédia dans le processus de l’application.

Les applications TAPI 3. x sont liées à Tapi3.dll.

 

 



