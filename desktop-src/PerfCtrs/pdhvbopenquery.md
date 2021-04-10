---
description: La fonction PdhVbOpenQuery crée et Initialise une structure de requête unique qui est utilisée pour gérer la collection de données de performances.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115562"
---
# <a name="pdhvbopenquery-function"></a>PdhVbOpenQuery fonction)

La fonction **PdhVbOpenQuery** crée et Initialise une structure de requête unique qui est utilisée pour gérer la collection de données de performances.

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbOpenQuery ( \_ ByVal QueryHandle As long \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variable qui est désactivée (est égal à 0) avant l’appel de la fonction et, si la fonction réussit, contient l’ID unique de la requête créée et ouverte. Ce handle est utilisé dans les appels suivants à d’autres fonctions PDH pour identifier la requête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne un entier **long** égal à \_ l’erreur Success et un nouveau handle dans la variable *QueryHandle* .

Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md). Les valeurs possibles sont les suivantes.



| Code de retour                                                                                                     | Description                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**PDH \_ argument non valide \_**</dt> </dl>           | L’argument n’est pas valide ou est incorrect.<br/>             |
| <dl> <dt>**\_échec d' \_ allocation de mémoire PDH \_**</dt> </dl> | Impossible d’allouer une mémoire tampon temporaire.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

