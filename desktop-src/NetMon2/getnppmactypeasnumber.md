---
description: Récupère le type MAC de la catégorie NetworkInfo de la section NPP de l’objet BLOB et convertit les données de type en un numéro de type MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: GetNPPMacTypeAsNumber, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525132"
---
# <a name="getnppmactypeasnumber-function"></a>GetNPPMacTypeAsNumber fonction)

La fonction **GetNPPMacTypeAsNumber** récupère le type Mac de la catégorie NetworkInfo de la section NPP de l’objet BLOB et convertit les données de type en un numéro de type Mac.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB spécifié.

</dd> <dt>

*lpMacType* \[ à\]
</dt> <dd>

Pointeur vers le type MAC.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la balise n’est pas disponible, la valeur de retour est de \_ type Mac \_ Unknown.

## <a name="remarks"></a>Notes

Cette fonction mappe la balise, **NPP : NetworkInfo : MacType** au **\_ type \_ \* Mac** , comme défini dans le fichier Npptypes. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




