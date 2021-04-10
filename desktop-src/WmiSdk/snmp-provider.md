---
description: Le fournisseur SNMP (simple Network Management Protocol) permet aux applications clientes d’accéder aux informations SNMP par le biais d’Windows Management Instrumentation (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI et SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210737"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="26c77-103">WMI et SNMP</span><span class="sxs-lookup"><span data-stu-id="26c77-103">WMI and SNMP</span></span>

<span data-ttu-id="26c77-104">Le fournisseur SNMP (simple Network Management Protocol) permet aux applications clientes d’accéder aux informations SNMP par le biais d’Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="26c77-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="26c77-105">Le fournisseur SNMP n’est pas installé par défaut.</span><span class="sxs-lookup"><span data-stu-id="26c77-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="26c77-106">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="26c77-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="26c77-107">Le protocole SNMP (simple Network Management Protocol) utilise un schéma pour définir des objets.</span><span class="sxs-lookup"><span data-stu-id="26c77-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="26c77-108">Le schéma est différent du schéma utilisé dans WMI.</span><span class="sxs-lookup"><span data-stu-id="26c77-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="26c77-109">Le schéma SNMPv1 et SNMPv2C est appelé la structure des informations de gestion (SMI) et est empaqueté en tant que fichiers MIB (Management Information base).</span><span class="sxs-lookup"><span data-stu-id="26c77-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="26c77-110">Les fichiers MIB définissent des objets à l’aide d’un langage standard, à savoir la notation de syntaxe abstraite 1 (ASN. 1), et un certain nombre de définitions de macros qui servent de modèles pour décrire les objets.</span><span class="sxs-lookup"><span data-stu-id="26c77-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="26c77-111">Les macros fournissent des informations telles que le nom de l’objet, l’identificateur, la syntaxe, la description, les droits d’accès, les opérations de protocole et l’encodage de protocole.</span><span class="sxs-lookup"><span data-stu-id="26c77-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="26c77-112">Le tableau suivant répertorie la manière dont le fournisseur SNMP gère les différents aspects d’un objet MIB.</span><span class="sxs-lookup"><span data-stu-id="26c77-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="26c77-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="26c77-113">Topic</span></span>                                                    | <span data-ttu-id="26c77-114">Description</span><span class="sxs-lookup"><span data-stu-id="26c77-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="26c77-115">Macro de TYPE NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="26c77-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="26c77-116">Mappage de la macro de **type notification** de SNMP à WMI.</span><span class="sxs-lookup"><span data-stu-id="26c77-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="26c77-117">Macro de TYPE objet</span><span class="sxs-lookup"><span data-stu-id="26c77-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="26c77-118">Mappage de la macro de **type objet** de SNMP à WMI.</span><span class="sxs-lookup"><span data-stu-id="26c77-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="26c77-119">Macro de CONVENTION textuelle</span><span class="sxs-lookup"><span data-stu-id="26c77-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="26c77-120">Comment la macro de **Convention textuelle** est mappée de SNMP à WMI.</span><span class="sxs-lookup"><span data-stu-id="26c77-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="26c77-121">TYPE d’interruption (macro)</span><span class="sxs-lookup"><span data-stu-id="26c77-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="26c77-122">Mappage de la macro de **type d’interruption** de SNMP à WMI.</span><span class="sxs-lookup"><span data-stu-id="26c77-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="26c77-123">Le fournisseur SNMP est fourni avec un compilateur qui traduit les objets MIB en objets WMI.</span><span class="sxs-lookup"><span data-stu-id="26c77-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="26c77-124">Le compilateur SNMP peut également générer des erreurs ou d’autres messages.</span><span class="sxs-lookup"><span data-stu-id="26c77-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="26c77-125">Pour plus d’informations, consultez [messages d’erreur du compilateur SNMP](snmp-compiler-error-messages.md) et [messages d’informations générales](general-information-messages.md).</span><span class="sxs-lookup"><span data-stu-id="26c77-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="26c77-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="26c77-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26c77-127">Référence WMI</span><span class="sxs-lookup"><span data-stu-id="26c77-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="26c77-128">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="26c77-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



