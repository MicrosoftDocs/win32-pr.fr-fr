---
description: La macro de TYPE NOTIFICATION contient les éléments suivants.
ms.assetid: b7c6ec2b-640b-4373-a1e3-ff6c130b07d0
ms.tgt_platform: multiple
title: Macro de TYPE NOTIFICATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2ff7695d7ca36eeaf01115d47df496d52d68ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529713"
---
# <a name="notification-type-macro"></a>Macro de TYPE NOTIFICATION

La macro de TYPE NOTIFICATION contient les éléments suivants.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Composants

<dl> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descripteur d’objet
</dt> <dd>

Joint un nom à un événement SNMP dans une macro de TYPE NOTIFICATION. La liste suivante répertorie les règles de mappage du descripteur d’objet.



| Type                        | Concatenate                                                                                                                                                                                                                                                                                                           |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom de classe CIM encapsulé | « SNMP \_ »<br/> Nom de l’identité du module MIB<br/> trait de soulignement ( \_ )<br/> descripteur d’objet<br/> « \_ Notification »<br/> Exemple : la notification **vtpServerDisabled** de **Cisco-VTP-MIB** est mappée à la **\_ notification SNMP Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_**.<br/>                 |
| Nom de la classe CIM référent     | « SNMP \_ »<br/> Nom de l’identité du module MIB<br/> trait de soulignement ( \_ )<br/> descripteur d’objet<br/> « \_ ExtendedNotification »<br/> Exemple : la notification **vtpServerDisabled** de **Cisco-VTP-MIB** est mappée à la valeur **SNMP \_ Cisco \_ VTP \_ MIB \_ vtpServerDisabled \_ ExtendedNotification**.<br/> |



 

</dd> <dt>

<span id="OBJECTS_clause"></span><span id="objects_clause"></span><span id="OBJECTS_CLAUSE"></span>Clause OBJECTs
</dt> <dd>

Énumère le jeu d’objets associés à l’objet de notification.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>RÉFÉRENCE (clause)
</dt> <dd>

Fait référence à un autre document qui contient plus d’informations sur l’objet. Elle est mappée à la **référence** de qualificateur de classe CIM, qui est de type chaîne.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION (clause)
</dt> <dd>

Décrit l’objet en question. Il correspond à la **Description** de qualificateur de classe CIM, qui est de type chaîne

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clause STATUs
</dt> <dd>

Indique si l’objet doit être pris en charge. Lorsque l’État est **obsolète** ou **déconseillé**, la notification est ignorée du mappage. Sinon, cette clause correspond à l' **État** du qualificateur de la classe CIM, qui est de type **chaîne**.

Pour SNMPv1, la valeur par défaut de l' **État** est **obligatoire** ou **facultative**, mais le qualificateur peut contenir une autre valeur. Pour SNMPv2C, la valeur par défaut de l' **État** est **en cours** ou **déconseillée**, mais le qualificateur peut contenir une autre valeur.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fournisseur SNMP mappe la macro de **type notification** à une définition de classe encapsulée ou référent.

Une définition de classe encapsulée n’expose pas les informations d’instance associées à l’objet MIB. Au lieu de cela, la définition de classe encode la clause OBJECTs sous la forme d’une série de propriétés de la classe d’événements CIM. Chaque propriété CIM reflète le nom, le type et la valeur de l’objet MIB correspondant dans la clause OBJECTs. Si vous avez besoin d’informations d’instance, vous devez mapper à une classe référent. Une définition de classe encapsulée est mappée à la classe [SnmpNotification](snmpnotification.md) .

Une classe référent définit un objet MIB et les informations d’instance utilisées pour obtenir l’objet. La définition de classe encode la clause OBJECTs sous la forme d’une série de propriétés de la classe d’événements CIM. Chaque propriété CIM reflète le nom de l’objet MIB correspondant dans la clause OBJECTs et le type en tant qu’objet incorporé qui reflète une instance de la classe associée à cet objet MIB. Le fournisseur génère ensuite une classe associée à l’objet MIB. Par exemple, **ifIndex** est mappé à une classe incorporée nommée **SNMP \_ RFC1213 \_ MIB \_ ifIndex**. Pour plus d’informations sur ce type de classe, consultez [macro de type objet](object-type-macro.md).

 

 




