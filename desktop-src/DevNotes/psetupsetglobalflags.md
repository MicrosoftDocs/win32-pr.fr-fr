---
description: Désactive les fonctionnalités.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535015"
---
# <a name="psetupsetglobalflags-function"></a>pSetupSetGlobalFlags fonction)

\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]

Désactive les fonctionnalités.

## <a name="syntax"></a>Syntaxe


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Indicateurs utilisés pour désactiver l’interface utilisateur ou la sauvegarde automatique.



| Valeur                                                                                                                                                                                                                                         | Signification                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_**</dt> <dt>0X004</dt> non interactif </dl> | Défini pour désactiver l’interface utilisateur.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ AUCUNE \_ sauvegarde**</dt> <dt>0x002</dt> </dl>               | Défini pour désactiver la sauvegarde automatique.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
