---
description: Utilise des appels séquentiels pour récupérer toutes les chaînes dans les plages spécifiées.
ms.assetid: 4e819975-84a5-4b73-9a19-792d3607da9c
title: GetStringsFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringsFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 25fbc149a663ef68d1588218937568401f414ef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950955"
---
# <a name="getstringsfromblob-function"></a>GetStringsFromBlob fonction)

La fonction **GetStringsFromBlob** utilise des appels séquentiels pour récupérer toutes les chaînes dans les plages spécifiées.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetStringsFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pRequestedOwnerName,
  _In_  const char  *pRequestedCategoryName,
  _In_  const char  *pRequestedTagName,
  _Out_ const char  **ppReturnedOwnerName,
  _Out_ const char  **ppReturnedCategoryName,
  _Out_ const char  **ppReturnedTagName,
  _Out_ const char  **ppReturnedString,
  _Out_       DWORD *pRestartKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB.

</dd> <dt>

*pRequestedOwnerName* \[ dans\]
</dt> <dd>

Pointeur vers la section propriétaire à partir de laquelle obtenir la chaîne.

</dd> <dt>

*pRequestedCategoryName* \[ dans\]
</dt> <dd>

Pointeur vers la section de catégorie à partir de laquelle obtenir la chaîne.

</dd> <dt>

*pRequestedTagName* \[ dans\]
</dt> <dd>

Pointeur vers la balise pour la chaîne demandée.

</dd> <dt>

*ppReturnedOwnerName* \[ à\]
</dt> <dd>

Pointeur vers la variable qui pointe vers l’emplacement où le nom du **propriétaire** sera retourné.

</dd> <dt>

*ppReturnedCategoryName* \[ à\]
</dt> <dd>

Pointeur vers la variable qui pointe vers l’emplacement où le nom de la **catégorie** sera retourné.

</dd> <dt>

*ppReturnedTagName* \[ à\]
</dt> <dd>

Pointeur vers la variable qui pointe vers l’emplacement où le nom de la **balise** sera retourné.

</dd> <dt>

*ppReturnedString* \[ à\]
</dt> <dd>

Pointeur vers la variable qui pointe vers l’emplacement où le nom de la chaîne sera retourné.

</dd> <dt>

*pRestartKey* \[ à\]
</dt> <dd>

Pointeur vers la variable où la clé de redémarrage sera spécifiée et retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique le problème.

Si une combinaison spécifiée d’informations de **propriétaire**, de **catégorie** et de **balise** n’existe pas, la valeur de retour est **NMERR l’entrée d' \_ objet BLOB \_ \_ n' \_ \_ existe pas**.

Lorsque l’objet BLOB est parcouru entièrement dans les limites initialement spécifiées, la fonction retourne **l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**, et le paramètre *pRestartKey* pointe sur zéro.

## <a name="remarks"></a>Notes

Lors de l’appel initial à la fonction **GetStringsFromBlob** , le paramètre *pRestartKey* pointe vers une variable qui contient la valeur zéro. Les paramètres préutilisés ne peuvent être utilisés que *si la clé* de redémarrage est égale à zéro. Dans les appels suivants, lorsque *pRestartKey* a une valeur *différente de zéro, les paramètres* prépriss sont ignorés. Lors de l’appel initial, tous les peuvent pointer vers la **valeur null**, qui définit la requête de sorte qu’elle retourne chaque entrée de l’objet BLOB, une par appel suivant.

La spécification d’un propriétaire limite les chaînes retournées uniquement à ce propriétaire. Une limitation similaire est vraie pour les catégories et les balises, avec un inconvénient supplémentaire : si une catégorie est spécifiée, un propriétaire doit également être spécifié et, si une balise est spécifiée, une catégorie (et donc un propriétaire) doit être spécifiée.

Lorsque l’appel initial à **GetStringsFromBlob** retourne, *pRestartKey* pointe vers une nouvelle valeur, qui doit être spécifiée lors de l’appel suivant à la fonction pour obtenir la valeur suivante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> </dl>

 

 




