---
description: Charge un pilote d’imprimante dans le magasin de pilotes des serveurs d’impression afin qu’il puisse être installé en appelant InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: UploadPrinterDriverPackage, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210085"
---
# <a name="uploadprinterdriverpackage-function"></a>UploadPrinterDriverPackage fonction)

Charge un pilote d’imprimante sur le magasin de pilotes du serveur d’impression afin qu’il puisse être installé en appelant [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression. Utilisez la **valeur null** si le serveur est l’ordinateur local.

</dd> <dt>

*pszInfPath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le chemin d’accès source au fichier. inf du pilote.

</dd> <dt>

*pszEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur du serveur (par exemple, Windows NT x86). Il peut s’agir de la **valeur null**.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Il peut s’agir de l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                     | Signification                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | L’interface utilisateur ne sera pas affichée pendant le téléchargement.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | Les fichiers sont téléchargés même si le package est déjà dans le magasin de pilotes du serveur.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | Le magasin de pilotes du serveur sera vérifié avant le chargement pour voir si le package existe déjà. Ce paramètre est ignoré si UPDP_UPLOAD_ALWAYS est défini.<br/> |



 

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de l’interface utilisateur de copie.

</dd> <dt>

*pszDestInfPath* \[ à\]
</dt> <dd>

Pointeur vers le chemin d’accès de destination, dans le magasin de pilotes, dans lequel le fichier. inf du pilote a été copié.

</dd> <dt>

*pcchDestInfPath* \[ in, out\]
</dt> <dd>

En entrée, spécifie la taille, en caractères, de la mémoire tampon *pszDestInfPath* . Lors de la sortie, reçoit la taille, en caractères, de la chaîne de chemin d’accès, y compris le caractère null de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est S_OK ; sinon, le **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Le magasin de pilotes est généralement% windir% \\ INF ou% windir% \\ system32 \\ DriverStore \\ FileRepository.

Un seul package à la fois peut être téléchargé. Si un package dépend d’autres, il doit être téléchargé séparément.

Seuls les packages de pilotes signés peuvent être téléchargés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **UploadPrinterDriverPackageW** (Unicode) et **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

