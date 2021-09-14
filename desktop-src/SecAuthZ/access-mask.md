---
description: Définit des droits standard, spécifiques et génériques. Ces droits sont utilisés dans les entrées de contrôle d’accès (ACE) et constituent le moyen principal de spécifier l’accès demandé ou accordé à un objet.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013753"
---
# <a name="access_mask"></a>masque d’accès \_

Le type de données **\_ masque d’accès** est une valeur **DWORD** qui définit des droits standard, spécifiques et génériques. Ces droits sont utilisés dans les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) et constituent le moyen principal de spécifier l’accès demandé ou accordé à un objet.


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a>Notes

Les bits de cette valeur sont alloués comme suit.



| Bits             | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 15<br/>  | Droits spécifiques. Contient le masque d’accès spécifique au type d’objet associé au masque.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| 16 23<br/> | Droits standard. Contient les droits d’accès standard de l’objet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 24<br/>    | Accédez à la sécurité du système (**accès à la \_ \_ sécurité du système**). Il est utilisé pour indiquer l’accès à une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL). ce type d’accès nécessite que le processus appelant dispose du **privilège \_ SE \_ nom de sécurité** (gérer le journal d’audit et de sécurité). Si cet indicateur est défini dans le masque d’accès d’une entrée de contrôle d’accès d’audit (succès ou échec de l’accès), l’accès à la liste SACL est audité.<br/> |
| 25<br/>    | Maximum autorisé (**maximum \_ autorisé**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 26 27<br/> | Réservé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| 28<br/>    | Générique tout (**générique \_ tout**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| 29<br/>    | Exécution générique (**\_ Exécution générique**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 30<br/>    | Écriture générique (**\_ écriture générique**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 31<br/>    | Lecture générique (**\_ lecture générique**).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

Les bits de droits standard, 16 à 23, contiennent les droits d’accès standard de l’objet et peuvent être une combinaison des indicateurs prédéfinis suivants.



| bit           | Indicateur                         | Signification                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 16<br/> | **DELETE**<br/>        | Supprimer l’accès.<br/>                                                                                                                                                                                                                |
| 17<br/> | **LIRE \_ le contrôle**<br/> | Accès en lecture au propriétaire, au groupe et à la [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) du descripteur de sécurité.<br/> |
| 18<br/> | **ÉCRITURE \_ DAC**<br/>    | Accès en écriture à la liste DACL.<br/>                                                                                                                                                                                                     |
| 19<br/> | **propriétaire en écriture \_**<br/>  | Accès en écriture au propriétaire.<br/>                                                                                                                                                                                                        |
| 20<br/> | **NON**<br/>   | Synchronisez l’accès.<br/>                                                                                                                                                                                                           |



 

Les constantes suivantes définies dans Winnt. h représentent les droits d’accès spécifiques et standard.


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>winnt. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle d’accès](access-control.md)
</dt> <dt>

[Structures de Access Control de base](authorization-structures.md)
</dt> <dt>

[Droits d’accès et masques d’accès](access-rights-and-access-masks.md)
</dt> <dt>

[**\_mappage générique**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

