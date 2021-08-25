---
title: Windows Constantes du collecteur d’événements (Evcoll. h)
description: le kit de développement logiciel (SDK) du collecteur d’événements Windows contient les constantes suivantes.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d168ecb16c293c524c4dffcb16aee7db2924e23219e42d402939ab26b4bbecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005979"
---
# <a name="windows-event-collector-constants"></a>Windows Constantes du collecteur d’événements

le kit de développement logiciel (SDK) du collecteur d’événements Windows contient les constantes suivantes.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_masque de \_ type de variante EC \_**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Utilisé pour masquer le bit du tableau de la propriété **type** d’une [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) pour extraire le type de la valeur variant.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_tableau de \_ type \_ Variant EC**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Lorsque ce bit est défini dans la propriété **type** d’un [**\_ Variant EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), le variant contient un pointeur vers un tableau de valeurs, plutôt que la valeur elle-même.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_accès en lecture EC \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Autorisation de lecture de contrôle d’accès qui permet la lecture d’informations à partir du collecteur d’événements.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_accès en écriture EC \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Autorisation écrire le contrôle d’accès qui permet d’écrire des informations dans le collecteur d’événements.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ Open \_ Always**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Ouvre un abonnement existant ou crée l’abonnement s’il n’existe pas. Utilisé par la méthode [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**\_création \_ de EC**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Indicateur passé à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) spécifiant qu’un nouvel abonnement doit être créé.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**\_Open EC \_ existant**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Indicateur passé à la fonction [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) spécifiant qu’un abonnement existant doit être ouvert.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





