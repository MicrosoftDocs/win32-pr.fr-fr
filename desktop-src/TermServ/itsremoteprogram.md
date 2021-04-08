---
title: Interface ITSRemoteProgram
description: Comprend des méthodes permettant de définir et de récupérer le mode RemoteApp et les paramètres de démarrage d’un programme RemoteApp, comme le chemin d’accès du fichier exécutable et le répertoire de travail.
ms.assetid: c9eec63b-7162-4bf8-b5d5-8cadb971ef98
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface ITSRemoteProgram
- Services Bureau à distance de l’interface ITSRemoteProgram, Description
topic_type:
- apiref
api_name:
- ITSRemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfec99c109dfd3f69e22caf13071b77cd41f61bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033001"
---
# <a name="itsremoteprogram-interface"></a>Interface ITSRemoteProgram

Comprend des méthodes permettant de définir et de récupérer le mode RemoteApp et les paramètres de démarrage d’un programme RemoteApp, comme le chemin d’accès du fichier exécutable et le répertoire de travail.

## <a name="members"></a>Membres

L’interface **ITSRemoteProgram** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITSRemoteProgram** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ITSRemoteProgram** possède ces méthodes.



| Méthode                                                            | Description                                                              |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**ServerStartProgram**](itsremoteprogram-serverstartprogram.md) | Spécifie un programme RemoteApp à démarrer dans la session à distance.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **ITSRemoteProgram** possède les propriétés suivantes.



| Propriété                                                                   | Type d’accès           | Description                    |
|:---------------------------------------------------------------------------|:----------------------|:-------------------------------|
| [**RemoteProgramMode**](itsremoteprogram-remoteprogrammode.md)<br/> | Lecture/écriture<br/> | Mode RemoteApp.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram est défini en tant que FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

