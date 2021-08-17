---
description: La fonction PdhVbAddCounter crée une entrée de compteur dans l’objet de requête spécifié et retourne un handle à ce compteur en cas de réussite.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6605e2fb02edad23831b22334b960eaa2e89f23206673608500f248452094ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061147"
---
# <a name="pdhvbaddcounter-function"></a>PdhVbAddCounter fonction)

La fonction **PdhVbAddCounter** crée une entrée de compteur dans l’objet de requête spécifié et retourne un handle à ce compteur en cas de réussite.

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbAddCounter ( \_ ByVal QueryHandle As long, \_ ByVal trajet As String, \_ ByVal CounterHandle As long \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*QueryHandle* 
</dt> <dd>

ID de la requête à laquelle ce compteur doit être assigné. Cette valeur est retournée par la fonction [**PdhVbOpenQuery**](pdhvbopenquery.md) .

</dd> <dt>

*CounterPath* 
</dt> <dd>

Chaîne de texte qui spécifie le nom du chemin d’accès au compteur à ajouter à la requête. Le contenu de cette chaîne doit être un chemin de compteur valide, tel qu’il est obtenu à partir de l’Explorateur de compteurs ou d’une autre source.

</dd> <dt>

*CounterHandle* 
</dt> <dd>

Référence unique qui identifie ce compteur dans la requête. Cette variable doit être initialisée à zéro avant que la fonction ne soit appelée. Elle contient une valeur valide lors du retour uniquement si la fonction se termine correctement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, elle retourne un entier **long** égal à \_ l’erreur Success et un nouveau handle dans la variable *CounterHandle* .

Si la fonction échoue, la valeur de retour est un [code d’erreur système](/windows/desktop/Debug/system-error-codes) ou un [code d’erreur PDH](pdh-error-codes.md). Les valeurs possibles sont les suivantes.



| Code de retour                                                                                                     | Description                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ argument non valide \_**</dt> </dl>           | Un ou plusieurs des arguments sont non valides ou incorrects.<br/>              |
| <dl> <dt>**\_échec d' \_ allocation de mémoire PDH \_**</dt> </dl> | Impossible d’allouer une mémoire tampon.<br/>                            |
| <dl> <dt>**\_handle PDH non valide \_**</dt> </dl>             | Le descripteur de requête n’est pas valide.<br/>                                     |
| <dl> <dt>**PDH \_ CSTATUS \_ aucun \_ compteur**</dt> </dl>        | Le compteur spécifié est introuvable.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ aucun \_ objet**</dt> </dl>         | L’objet spécifié est introuvable.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ aucun \_ ordinateur**</dt> </dl>        | Une entrée d’ordinateur n’a pas pu être créée.<br/>                             |
| <dl> <dt>**PDH \_ CSTATUS \_ , \_ COUNTERNAME incorrect**</dt> </dl>   | Une chaîne de chemin d’accès de nom de compteur vide a été transmise.<br/>                   |
| <dl> <dt>**\_fonction PDH \_ \_ introuvable**</dt> </dl>        | La fonction de calcul de ce compteur n’a pas pu être déterminée.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

