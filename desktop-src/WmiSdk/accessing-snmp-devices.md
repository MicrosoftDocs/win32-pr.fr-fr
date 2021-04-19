---
description: Permet aux applications clientes d’accéder aux informations SNMP via WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Accès aux appareils SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538384"
---
# <a name="accessing-snmp-devices"></a><span data-ttu-id="cc07f-103">Accès aux appareils SNMP</span><span class="sxs-lookup"><span data-stu-id="cc07f-103">Accessing SNMP Devices</span></span>

<span data-ttu-id="cc07f-104">Le fournisseur SNMP (simple Network Management Protocol) permet aux applications clientes d’accéder aux informations SNMP via WMI.</span><span class="sxs-lookup"><span data-stu-id="cc07f-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through WMI.</span></span> <span data-ttu-id="cc07f-105">Le [fournisseur SNMP](snmp-provider.md) joue le rôle de passerelle pour les systèmes et les périphériques qui utilisent SNMP pour la gestion.</span><span class="sxs-lookup"><span data-stu-id="cc07f-105">The [SNMP provider](snmp-provider.md) acts as a gateway to systems and devices that use SNMP for management.</span></span> <span data-ttu-id="cc07f-106">Seul l’ordinateur de gestion ou de surveillance doit exécuter WMI, car il peut lire à partir de n’importe quel périphérique compatible SNMP.</span><span class="sxs-lookup"><span data-stu-id="cc07f-106">Only the management or monitoring computer must be running WMI because it can read from any SNMP-enabled device.</span></span>

> [!Note]  
> <span data-ttu-id="cc07f-107">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cc07f-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="cc07f-108">Les variables d’objet MIB (Management Information base) SNMP peuvent être lues et écrites, et les interruptions SNMP peuvent être mappées automatiquement aux événements WMI, qui peuvent être définies pour des opérations de création, de suppression ou de mise à jour arbitraires sur des données au-delà des interruptions définies par la MIB.</span><span class="sxs-lookup"><span data-stu-id="cc07f-108">SNMP Management Information Base (MIB) object variables can be read from and written to, and SNMP traps can be automatically mapped to WMI events, which can be defined for any arbitrary create, delete, or update operations to data beyond the MIB-defined traps.</span></span> <span data-ttu-id="cc07f-109">Cette fonctionnalité de WMI fonctionne comme une extension des fonctionnalités SNMP standard.</span><span class="sxs-lookup"><span data-stu-id="cc07f-109">This feature of WMI functions as an extension of standard SNMP capabilities.</span></span> <span data-ttu-id="cc07f-110">Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="cc07f-110">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

<span data-ttu-id="cc07f-111">Les outils décrits dans les rubriques suivantes sont conçus pour être utilisés par les programmeurs Windows Scripting et C/C++.</span><span class="sxs-lookup"><span data-stu-id="cc07f-111">The tools described in the following topics are designed for use by Windows scripting and C/C++ programmers.</span></span> <span data-ttu-id="cc07f-112">Il est recommandé de vous familiariser avec WMI, SNMPv1 et SNMPv2C, ainsi que des connaissances pratiques sur les concepts de gestion réseau et de réseau.</span><span class="sxs-lookup"><span data-stu-id="cc07f-112">Familiarity with WMI, SNMPv1 and SNMPv2C, and a working knowledge of networking and network management concepts are recommended.</span></span>

<span data-ttu-id="cc07f-113">Pour plus d’informations sur l’utilisation de WMI avec SNMP, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cc07f-113">For more information about using WMI with SNMP, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

 



