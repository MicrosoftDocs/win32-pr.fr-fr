---
description: Glossaire des termes de Moniteur réseau qui commencent par la lettre P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 321398fb-683f-4fb1-b6b7-c7826811cacd
title: P (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a95ed739acb6f4a59cf8c7a7edb760547f6469
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194591"
---
# <a name="p-network-monitor"></a>P (Moniteur réseau)

<dl> <dt>

<span id="_netmon_packet_gly"></span><span id="_NETMON_PACKET_GLY"></span>**paquet**
</dt> <dd>

Consultez [*Frame*](f.md).

</dd> <dt>

<span id="_netmon_parser_gly"></span><span id="_NETMON_PARSER_GLY"></span>**analyseur**
</dt> <dd>

Composant qui détecte un protocole spécifique dans une capture retardée. Chaque analyseur peut détecter un protocole. Toutefois, une DLL d’analyseur peut contenir plusieurs analyseurs. Également appelé analyseur de protocole.

</dd> <dt>

<span id="_netmon_parser.ini_gly"></span><span id="_NETMON_PARSER.INI_GLY"></span>**parser.ini**
</dt> <dd>

Fichier d’initialisation Moniteur réseau qui contient une liste de tous les analyseurs installés. Pour chaque analyseur, il existe une chaîne de commentaire qui décrit l’analyseur, le jeu suivant de l’analyseur et tout fichier d’aide associé à l’analyseur. Le fichier INI de l’analyseur est mis à jour lorsque Moniteur réseau appelle **ParserAutoInstallInfo** ou lorsque la dll de l’analyseur appelle **CreateHandoffTable**.

</dd> <dt>

<span id="_netmon_perfmon_gly"></span><span id="_NETMON_PERFMON_GLY"></span>**Analyse**
</dt> <dd>

Outil logiciel qui vous permet d’afficher les variables liées aux performances réseau qui identifient l’activité d’un processus.

</dd> <dt>

<span id="_netmon_promiscuous_mode_gly"></span><span id="_NETMON_PROMISCUOUS_MODE_GLY"></span>**mode promiscuité**
</dt> <dd>

État dans lequel une carte réseau copie toutes les trames transmises sur le réseau, quelle que soit l’adresse de destination dans une mémoire tampon locale. Ce mode permet à Moniteur réseau de capturer et d’afficher tout le trafic réseau.

</dd> <dt>

<span id="_netmon_property_gly"></span><span id="_NETMON_PROPERTY_GLY"></span>**propriété**
</dt> <dd>

Élément de protocole dans un analyseur qui décrit un champ de données dans un frame qui est envoyé à l’aide de ce protocole.

</dd> <dt>

<span id="_netmon_property_database_gly"></span><span id="_NETMON_PROPERTY_DATABASE_GLY"></span>**base de données de propriétés**
</dt> <dd>

Base de données interne qui définit toutes les propriétés prises en charge par un protocole spécifique. La base de données de propriétés contient une structure **PROPERTYINFO** pour chaque propriété définie par l’analyseur. Moniteur réseau utilise les informations de la base de données lorsqu’il attache une définition de propriété à une instance de la propriété, et lorsqu’il met en forme les données de propriété qui s’affichent dans le volet d’informations de l’interface utilisateur Moniteur réseau.

</dd> <dt>

<span id="_netmon_protocol_level_gly"></span><span id="_NETMON_PROTOCOL_LEVEL_GLY"></span>**niveau de protocole**
</dt> <dd>

Regroupement logique des propriétés de protocole.

</dd> </dl>

 

 



