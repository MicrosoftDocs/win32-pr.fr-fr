---
title: Méthode ITSRemoteProgram ServerStartProgram
description: Spécifie un programme RemoteApp à démarrer dans la session à distance.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ServerStartProgram
- Méthode ServerStartProgram Services Bureau à distance, interface ITSRemoteProgram
- Services Bureau à distance de l’interface ITSRemoteProgram, méthode ServerStartProgram
- Méthode ServerStartProgram Services Bureau à distance, interface ITSRemoteProgram2
- Services Bureau à distance de l’interface ITSRemoteProgram2, méthode ServerStartProgram
- Méthode ServerStartProgram Services Bureau à distance, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, méthode ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508753"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>ITSRemoteProgram :: ServerStartProgram, méthode

Spécifie un programme RemoteApp à démarrer dans la session à distance. Cette fonction doit être appelée dans une session connectée (après la réception de la notification de session connectée au client). Un nombre quelconque de programmes RemoteApp peuvent être démarrés dans une session. Une session RemoteApp expire si aucun programme RemoteApp n’est démarré dans la session dans le délai imparti, soit deux minutes pour Windows Server 2008.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrExecutablePath* \[ dans\]
</dt> <dd>

Chemin d’accès du fichier exécutable du programme RemoteApp sur le serveur.

</dd> <dt>

*bstrFilePath* \[ dans\]
</dt> <dd>

Chemin d’accès d’un fichier à ouvrir sur le serveur par le biais d’une association de fichier, par exemple « C : \\ \\ documents \\ \\MyReport.docx ». Si vous spécifiez *bstrFilePath*, vous ne devez pas spécifier le paramètre *bstrExecutablePath* , et vice versa. Vous devez uniquement spécifier l’un des paramètres.

</dd> <dt>

*bstrWorkingDirectory* \[ dans\]
</dt> <dd>

Répertoire de travail sur le serveur pour le programme RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ dans\]
</dt> <dd>

Indique si le serveur doit développer les variables d’environnement dans le chemin d’accès du répertoire de travail. Affectez à ce paramètre la **\_ valeur variant true** si le chemin d’accès du répertoire de travail contient des variables d’environnement ou **\_ false** si le chemin d’accès du répertoire de travail ne contient pas de variables d’environnement.

</dd> <dt>

*bstrArguments* \[ dans\]
</dt> <dd>

Arguments de ligne de commande pour le programme RemoteApp spécifiés dans *bstrExecutablePath*. Affectez la valeur **null** si *bstrExecutablePath* n’est pas spécifié.

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ dans\]
</dt> <dd>

Indique si le serveur doit développer les variables d’environnement dans les arguments de ligne de commande. Affectez à ce paramètre la **\_ valeur variant true** si les arguments contiennent des variables d’environnement, ou **\_ false** si les arguments ne contiennent pas de variables d’environnement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

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

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





