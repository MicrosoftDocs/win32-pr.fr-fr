---
title: Identificateurs d’objets (SNMP)
description: Un identificateur d’objet SNMP désigne un objet de manière unique et identifie son emplacement dans une arborescence de base d’informations de gestion (MIB).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81d52e43cb3be89551dd597bc5084d533f3913264f8bcf5c0a2ef7dbb375bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009257"
---
# <a name="object-identifiers-snmp"></a>Identificateurs d’objets (SNMP)

Un identificateur d’objet SNMP désigne un objet de manière unique et identifie son emplacement dans une arborescence de base d’informations de gestion (MIB). Les identificateurs d’objet sont des types de données ASN. 1 (Abstract Syntax Notation One) indépendants de l’application qui se composent d’une séquence d’entiers non négatifs ou de sous-identificateurs. Les identificateurs d’objet doivent avoir au moins deux sous-identificateurs et ne doivent pas dépasser 128 sous-identificateurs.

L’environnement de programmation WinSNMP utilise la structure [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) pour gérer les identificateurs d’objets. Le format du tableau d’identificateur d’objet dans une structure **smiOID** est un sous-identificateur par élément de tableau.

La représentation sous forme de chaîne numérique en pointillés d’un identificateur d’objet sépare ses sous-identificateurs par des points ; par exemple, « 1.2.3.4.5.6 ».

Pour plus d’informations, consultez [la base de données MIB (Management Information base) SNMP](the-snmp-management-information-base-mib-.md) et les RFC correspondants.

 

 




