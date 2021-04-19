---
description: Les fournisseurs d’événements SNMP reçoivent les paquets d’événements SNMP de la pile WINSNMP et traduisent les informations incluses dans les paquets en événements WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Choix entre des fournisseurs d’événements SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534661"
---
# <a name="choosing-between-snmp-event-providers"></a><span data-ttu-id="ea4d5-103">Choix entre des fournisseurs d’événements SNMP</span><span class="sxs-lookup"><span data-stu-id="ea4d5-103">Choosing Between SNMP Event Providers</span></span>

<span data-ttu-id="ea4d5-104">Les fournisseurs d’événements SNMP reçoivent les paquets d’événements SNMP de la pile WINSNMP et traduisent les informations incluses dans les paquets en événements WMI.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-104">SNMP event providers receive SNMP event packets from the WINSNMP stack and translate the information included in the packets into WMI events.</span></span>

<span data-ttu-id="ea4d5-105">WMI comprend les deux fournisseurs d’événements SNMP suivants :</span><span class="sxs-lookup"><span data-stu-id="ea4d5-105">WMI includes the following two SNMP event providers:</span></span>

-   <span data-ttu-id="ea4d5-106">Fournisseur d’événements encapsulés SNMP (SEEP)</span><span class="sxs-lookup"><span data-stu-id="ea4d5-106">SNMP Encapsulated Event provider (SEEP)</span></span>

    <span data-ttu-id="ea4d5-107">L’approvisionnement encapsulé signifie que l’instance d’événement a des propriétés simples qui décrivent les informations mappées directement à partir de l’interruption SNMP.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-107">Encapsulated provision means that the event instance has simple properties describing the information mapped directly from the SNMP trap.</span></span>

-   <span data-ttu-id="ea4d5-108">Fournisseur d’événements référent SNMP (SREP)</span><span class="sxs-lookup"><span data-stu-id="ea4d5-108">SNMP Referent Event provider (SREP)</span></span>

    <span data-ttu-id="ea4d5-109">Le service référent extrait les informations présentes dans l’interruption SNMP afin que les propriétés qui partagent la même classe et l’instance soient présentées sous forme d’objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-109">Referent provision abstracts the information present within the SNMP trap so that properties which share the same class and instance are presented as embedded objects.</span></span> <span data-ttu-id="ea4d5-110">Cela permet à l’instance unique, à laquelle l’interruption est associée, d’être récupérée après la réception de l’événement, à l’aide du \_ \_ RelPath SNMP.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-110">This allows for the unique instance, with which the trap is associated, to be retrieved after the receipt of the event, using the SNMP \_\_RELPATH.</span></span>

> [!Note]  
> <span data-ttu-id="ea4d5-111">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ea4d5-111">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="ea4d5-112">Indépendamment du fait que l’événement SNMP soit une notification SNMPv1 ou SNMPv2C, la pile le signale comme une notification SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-112">Regardless of whether the SNMP event is an SNMPv1 trap or an SNMPv2C notification, the stack reports it as an SNMPv2 notification.</span></span> <span data-ttu-id="ea4d5-113">Par conséquent, les fournisseurs d’événements traitent tous les événements SNMP en tant que notifications SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-113">Therefore, the event providers process all SNMP events as SNMPv2 notifications.</span></span>

<span data-ttu-id="ea4d5-114">Pour décrire les événements SNMP aux consommateurs WMI, chaque fournisseur d’événements prend en charge une hiérarchie de classes qui dérive de la classe système [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="ea4d5-114">To describe the SNMP events to WMI consumers, each event provider supports a hierarchy of classes that derives from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) system class.</span></span> <span data-ttu-id="ea4d5-115">La classe [SNMPNotification](snmpnotification.md) est la classe parente de la hiérarchie SEEP ; la classe [SNMPExtendedNotification](snmpextendednotification.md) est la classe parente de la hiérarchie SREP.</span><span class="sxs-lookup"><span data-stu-id="ea4d5-115">The [SNMPNotification](snmpnotification.md) class is the parent class for the SEEP hierarchy; the [SNMPExtendedNotification](snmpextendednotification.md) class is the parent class for the SREP hierarchy.</span></span>

 

 



