---
description: Cette API est réservée à un usage interne et ne doit pas être utilisée dans votre code.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: ApiSetQueryApiSetPresence, fonction (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527716"
---
# <a name="apisetqueryapisetpresence-function"></a>ApiSetQueryApiSetPresence fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Cette API est réservée à un usage interne et ne doit pas être utilisée dans votre code.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Espace de noms* \[ dans\]
</dt> <dd></dd> <dt>

*Présent* \[ à\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                                                                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                                                                                                                  |
| En-tête<br/>                   | <dl> <dt>Apiquery. h</dt> </dl>                                                                                                                 |
| Bibliothèque<br/>                  | <dl> <dt>API-MS-Win-Core-apiquery-L1. lib ; </dt> <dt>API-MS-Win-Core-apiquery-L1-1 1/-0. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt> </dl>                                                                                        |



 

 




