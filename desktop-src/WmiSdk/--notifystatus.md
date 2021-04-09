---
description: Sert de classe parente pour les classes d’erreur définies par le fournisseur.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Classe __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759441"
---
# <a name="__notifystatus-class"></a>\_\_NotifyStatus, classe

La classe système abstraite **\_ \_ NotifyStatus** sert de classe parente pour les classes d’erreur définies par le fournisseur.

La syntaxe suivante est simplifiée du code format MOF (MF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ NotifyStatus** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ NotifyStatus** possède les propriétés suivantes.

<dl> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contient une erreur ou un code d’information pour une opération. Il peut s’agir de n’importe quel code défini par l’utilisateur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite de l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

Bien que la classe **\_ \_ NotifyStatus** puisse être la classe parente pour les classes d’erreur définies par le fournisseur, il est recommandé que les fournisseurs dérivent les classes d’erreur de [**\_ \_ ExtendedStatus**](--extendedstatus.md) à la place. L’utilisation de **\_ \_ ExtendedStatus** permet une plus grande normalisation des classes d’erreur.

Les fournisseurs ne doivent jamais créer des instances de **\_ \_ NotifyStatus** directement, car ces instances ne transmettent pas plus d’informations qu’un simple code de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> </dl>

 

 




