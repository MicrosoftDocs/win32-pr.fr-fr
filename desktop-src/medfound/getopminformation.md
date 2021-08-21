---
description: Envoie une demande d’État OPM à un objet de sortie protégé.
ms.assetid: 4b691b20-25de-4b9e-a725-674a57697b56
title: GetOPMInformation fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bd9912289d17085bf94f3ef8316869ffb29d3a5adead4e10fc0e6d24844f4ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777299"
---
# <a name="getopminformation-function"></a>GetOPMInformation fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Envoie une demande d’État OPM à un objet de sortie protégé.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI GetOPMInformation(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE       opoOPMProtectedOutput,
  _In_  const DXGKMDT_OPM_GET_INFO_PARAMETERS   *pParameters,
  _Out_       DXGKMDT_OPM_REQUESTED_INFORMATION *pRequestedInformation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*opoOPMProtectedOutput* \[ dans\]
</dt> <dd>

Handle de l’objet de sortie protégé. Ce handle est obtenu en appelant [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

</dd> <dt>

*pParameters* \[ dans\]
</dt> <dd>

Pointeur vers une structure **de \_ paramètres d' \_ obtenir des \_ informations \_ DXGKMDT OPM** qui contient des données d’entrée pour la demande d’État.

</dd> <dt>

*pRequestedInformation* \[ à\]
</dt> <dd>

Pointeur vers une structure **d' \_ \_ \_ informations DXGKMDT OPM demandée** qui reçoit les résultats de la demande d’État.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Remarques

Les applications doivent appeler [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) au lieu d’appeler cette fonction.

L’objet de sortie protégé doit être créé avec la sémantique OPM. Consultez [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions OPM](opm-functions.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 
