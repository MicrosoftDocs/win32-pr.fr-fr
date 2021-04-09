---
Description: Récupère les données de la base de données des détails AppHelp.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: SdbReadApphelpDetailsData fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942062"
---
# <a name="sdbreadapphelpdetailsdata-function"></a>SdbReadApphelpDetailsData fonction)

Récupère les données de la base de données des détails AppHelp.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Un descripteur de la base de données de détails AppHelp, AppHelp. sdb.

</dd> <dt>

*pData* \[ à\]
</dt> <dd>

Structure [**de \_ données APPHELP**](apphelp-data.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




