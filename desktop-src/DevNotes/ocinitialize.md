---
description: Initialise le gestionnaire de composants facultatif.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540220"
---
# <a name="ocinitialize-function"></a>OcInitialize fonction)

Initialise le gestionnaire de composants facultatif.

## <a name="syntax"></a>Syntaxe


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Rappels* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ rappels de client OCM**](ocm-client-callbacks.md) qui spécifie les fonctions de rappel que le gestionnaire OC doit utiliser pour effectuer diverses tâches.

</dd> <dt>

*MasterOcInfName* \[ dans\]
</dt> <dd>

Chemin d’accès du fichier. inf OC maître.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Ce paramètre peut être une ou plusieurs des valeurs suivantes.

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)
</dt> </dl> </dd> <dt>

*ShowError* \[ à\]
</dt> <dd>

Si la fonction échoue, ce paramètre indique s’il faut afficher un message d’erreur.

</dd> <dt>

*Journal* \[ dans\]
</dt> <dd>

Handle du journal.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne la valeur de contexte du gestionnaire OC.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_rappels de client OCM \_**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
