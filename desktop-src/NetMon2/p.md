---
description: Glossaire des termes de Moniteur réseau qui commencent par la lettre P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034085"
---
# <a name="p-network-monitor"></a><span data-ttu-id="0034d-103">P (Moniteur réseau)</span><span class="sxs-lookup"><span data-stu-id="0034d-103">P (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="0034d-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**paquet**</span><span class="sxs-lookup"><span data-stu-id="0034d-104"><span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**packet**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-105">Consultez [*Frame*](f.md).</span><span class="sxs-lookup"><span data-stu-id="0034d-105">See [*frame*](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="0034d-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**analyseur**</span><span class="sxs-lookup"><span data-stu-id="0034d-106"><span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**parser**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-107">Composant qui détecte un protocole spécifique dans une capture retardée.</span><span class="sxs-lookup"><span data-stu-id="0034d-107">A component that detects a specific protocol in a delayed capture.</span></span> <span data-ttu-id="0034d-108">Chaque analyseur peut détecter un protocole.</span><span class="sxs-lookup"><span data-stu-id="0034d-108">Each parser can detect one protocol.</span></span> <span data-ttu-id="0034d-109">Toutefois, une DLL d’analyseur peut contenir plusieurs analyseurs.</span><span class="sxs-lookup"><span data-stu-id="0034d-109">However, one parser DLL may contain multiple parsers.</span></span> <span data-ttu-id="0034d-110">Également appelé analyseur de protocole.</span><span class="sxs-lookup"><span data-stu-id="0034d-110">Also called a protocol parser.</span></span>

</dd> <dt>

<span data-ttu-id="0034d-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span><span class="sxs-lookup"><span data-stu-id="0034d-111"><span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-112">Fichier d’initialisation Moniteur réseau qui contient une liste de tous les analyseurs installés.</span><span class="sxs-lookup"><span data-stu-id="0034d-112">A Network Monitor initialization file that contains a list of all the installed parsers.</span></span> <span data-ttu-id="0034d-113">Pour chaque analyseur, il existe une chaîne de commentaire qui décrit l’analyseur, le jeu suivant de l’analyseur et tout fichier d’aide associé à l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="0034d-113">For each parser there is a comment string that describes the parser, the follow set of the parser, and any Help file associated with the parser.</span></span> <span data-ttu-id="0034d-114">Le fichier INI de l’analyseur est mis à jour lorsque Moniteur réseau appelle **ParserAutoInstallInfo** ou lorsque la dll de l’analyseur appelle **CreateHandoffTable**.</span><span class="sxs-lookup"><span data-stu-id="0034d-114">The parser INI file is updated when Network Monitor calls **ParserAutoInstallInfo**, or when the parser DLL calls **CreateHandoffTable**.</span></span>

</dd> <dt>

<span data-ttu-id="0034d-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Analyse**</span><span class="sxs-lookup"><span data-stu-id="0034d-115"><span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Perfmon**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-116">Outil logiciel qui vous permet d’afficher les variables liées aux performances réseau qui identifient l’activité d’un processus.</span><span class="sxs-lookup"><span data-stu-id="0034d-116">A software tool that allows you to view network performance-related variables that identify the activity of a process.</span></span>

</dd> <dt>

<span data-ttu-id="0034d-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**mode promiscuité**</span><span class="sxs-lookup"><span data-stu-id="0034d-117"><span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**promiscuous mode**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-118">État dans lequel une carte réseau copie toutes les trames transmises sur le réseau, quelle que soit l’adresse de destination dans une mémoire tampon locale.</span><span class="sxs-lookup"><span data-stu-id="0034d-118">A state in which a network adapter card copies all the frames that pass over the network, regardless of the destination address to a local buffer.</span></span> <span data-ttu-id="0034d-119">Ce mode permet à Moniteur réseau de capturer et d’afficher tout le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="0034d-119">This mode enables Network Monitor to capture and display all network traffic.</span></span>

</dd> <dt>

<span data-ttu-id="0034d-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**propriété**</span><span class="sxs-lookup"><span data-stu-id="0034d-120"><span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**property**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-121">Élément de protocole dans un analyseur qui décrit un champ de données dans un frame qui est envoyé à l’aide de ce protocole.</span><span class="sxs-lookup"><span data-stu-id="0034d-121">A protocol element in a parser that describes a data field within a frame that is sent by using that protocol.</span></span>

</dd> <dt>

<span data-ttu-id="0034d-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**base de données de propriétés**</span><span class="sxs-lookup"><span data-stu-id="0034d-122"><span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**property database**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-123">Base de données interne qui définit toutes les propriétés prises en charge par un protocole spécifique.</span><span class="sxs-lookup"><span data-stu-id="0034d-123">An internal database that defines all the properties that a specific protocol supports.</span></span> <span data-ttu-id="0034d-124">La base de données de propriétés contient une structure **PROPERTYINFO** pour chaque propriété définie par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="0034d-124">The property database contains a **PROPERTYINFO** structure for each property that the parser defines.</span></span> <span data-ttu-id="0034d-125">Moniteur réseau utilise les informations de la base de données lorsqu’il attache une définition de propriété à une instance de la propriété, et lorsqu’il met en forme les données de propriété qui s’affichent dans le volet d’informations de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="0034d-125">Network Monitor uses the information in the database when it attaches a property definition to an instance of the property, and when it formats the property data that is displayed in the details pane of the Network Monitor UI.</span></span>

</dd> <dt>

<span data-ttu-id="0034d-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**niveau de protocole**</span><span class="sxs-lookup"><span data-stu-id="0034d-126"><span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**protocol level**</span></span>
</dt> <dd>

<span data-ttu-id="0034d-127">Regroupement logique des propriétés de protocole.</span><span class="sxs-lookup"><span data-stu-id="0034d-127">A logical grouping of protocol properties.</span></span>

</dd> </dl>

 

 



