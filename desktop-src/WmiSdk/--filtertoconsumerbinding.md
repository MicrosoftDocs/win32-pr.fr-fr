---
description: Est utilisé dans l’inscription des consommateurs d’événements permanents pour associer une instance de \_ \_ EventConsumer à une instance de \_ \_ EventFilter.
ms.assetid: e6a06161-0f1c-4754-ac34-263ccf7bf10d
ms.tgt_platform: multiple
title: Classe __FilterToConsumerBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __FilterToConsumerBinding
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58196a18a0894b12b6e43a963834f324503e974338d4dec78b01ac6850d66859
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926187"
---
# <a name="__filtertoconsumerbinding-class"></a>\_\_FilterToConsumerBinding, classe

La classe système **\_ \_ FilterToConsumerBinding** est utilisée dans l’inscription des consommateurs d’événements permanents pour associer une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) à une instance de [**\_ \_ EventFilter**](--eventfilter.md).**\_ \_ FilterToConsumerBinding** est une classe d’association.

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class __FilterToConsumerBinding : __IndicationRelated
{
  __EventConsumer REF Consumer;
  uint8               CreatorSID[];
  boolean             DeliverSynchronously = False;
  uint32              DeliveryQoS;
  __EventFilter   REF Filter;
  boolean             MaintainSecurityContext = False;
  boolean             SlowDownProviders = False;
};
```

## <a name="members"></a>Membres

La classe **\_ \_ FilterToConsumerBinding** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **\_ \_ FilterToConsumerBinding** possède les propriétés suivantes.

<dl> <dt>

**Consommateur**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ EventConsumer**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Référence à une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) qui représente le chemin d’accès de l’objet à un consommateur logique, le destinataire d’un événement. Un consommateur logique est une instance d’une classe dérivée de **\_ \_ EventConsumer**.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui a créé la liaison. Selon le système d’exploitation, WMI stocke le SID de l’administrateur ou le SID de l’utilisateur qui crée une instance de **\_ \_ FilterToConsumerBinding**. Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**DeliverSynchronously**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Obsolète. Utilisez plutôt la propriété **DeliveryQoS** à la place de cette propriété, car si **DeliverSynchronously** est défini sur **true** , il remplace le paramètre de la propriété **DeliveryQoS** .

</dd> <dt>

**DeliveryQoS**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Qualité de service pour un abonnement. Si la propriété **DeliverSynchronously** est définie sur **true**, elle remplace la valeur de la propriété **DeliveryQoS** .

<dt>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>

<span id="WMIMSG_FLAG_QOS_SYNCHRONOUS"></span><span id="wmimsg_flag_qos_synchronous"></span>**WMIMSG \_ INDICATEUR de \_ QoS \_ synchrone** (0)


</dt> <dd>

Remise synchrone

**Faux**. L’événement est remis au consommateur logique de façon synchrone.

</dd> <dt>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>

<span id="WMIMSG_FLAG_QOS_EXPRESS"></span><span id="wmimsg_flag_qos_express"></span>**WMIMSG \_ INDICATEUR \_ QoS \_ Express** (1)


</dt> <dd>

Livraison express

**Vrai**. L’événement est remis au consommateur logique de manière asynchrone.

</dd> </dl>

</dd> <dt>

**Filter**
</dt> <dd> <dl> <dt>

Type de données : **\_ \_ EventFilter**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> <dt>

Qualificateurs : [ **clé**](standard-qualifiers.md)
</dt> </dl>

Référence à une instance de [**\_ \_ EventFilter**](--eventfilter.md) qui représente le chemin d’accès de l’objet à un filtre d’événement qui est une requête qui spécifie le type d’événement à recevoir.

</dd> <dt>

**MaintainSecurityContext**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, les événements sont remis dans le contexte de sécurité dans lequel se trouvait le fournisseur lorsqu’il les a fournies.

> [!Note]  
> Seul un consommateur implémenté en tant que DLL (un consommateur in-process) peut recevoir des événements dans le contexte de sécurité du fournisseur. Pour plus d’informations sur la sécurité et les fournisseurs in-process, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md). Pour plus d’informations et pour obtenir des exemples, consultez remplacement :[réception d’événements en toute sécurité](receiving-events-securely.md).

 

</dd> <dt>

**SlowDownProviders**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Si la **valeur est true**, les fournisseurs sont ralentis si ce consommateur ne peut pas continuer.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **\_ \_ FilterToConsumerBinding** est dérivée de [**\_ \_ IndicationRelated**](--indicationrelated.md), qui n’a pas de propriétés.

Les consommateurs d’événements permanents utilisent la classe système **\_ \_ FilterToConsumerBinding** pour lier les filtres d’événements aux consommateurs finaux. Une fois que le filtre et le consommateur sont liés, WMI peut transférer les événements qui correspondent au filtre au consommateur correspondant.

## <a name="examples"></a>Exemples

L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **\_ \_ FilterToConsumerBinding** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |
| Espace de noms<br/>                | Tous les espaces de noms WMI<br/>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_\_IndicationRelated**](--indicationrelated.md)
</dt> <dt>

[Classes système WMI](wmi-system-classes.md)
</dt> <dt>

[Surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Événements d’analyse](monitoring-events.md)
</dt> <dt>

[Création d’un filtre d’événements](creating-an-event-filter.md)
</dt> <dt>

[Sécurisation des événements WMI](securing-wmi-events.md)
</dt> </dl>

 

 




