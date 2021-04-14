---
description: Configure un objet de sortie protégé.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: ConfigureOPMProtectedOutput fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393299"
---
# <a name="configureopmprotectedoutput-function"></a>ConfigureOPMProtectedOutput fonction)

> [!IMPORTANT]
> Cette fonction est utilisée par [Output Protection Manager](output-protection-manager.md) (OPM) pour accéder aux fonctionnalités dans le pilote d’affichage. Les applications ne doivent pas appeler cette fonction.

 

Configure un objet de sortie protégé.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
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

Pointeur vers une structure **de \_ \_ \_ paramètres OPM DXGKMDT configure** qui contient la commande de configuration.

</dd> <dt>

*ulAdditionalParametersSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *pbAdditionalParameters* , en octets.

</dd> <dt>

*pbAdditionalParameters* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient des informations supplémentaires pour la commande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, elle retourne l' **état \_ Success**. Sinon, elle retourne un code d’erreur **NTSTATUS** .

## <a name="remarks"></a>Notes

Les applications doivent appeler [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) au lieu d’appeler cette fonction.

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Gdi32.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions OPM](opm-functions.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> </dl>

 

 
