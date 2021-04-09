---
description: 'En savoir plus sur : moteur de stockage extensible'
title: Moteur de stockage extensible
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0ef85de696f52d2220c11b05ed7ada76a70df871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034167"
---
# <a name="extensible-storage-engine"></a>Moteur de stockage extensible


_**S’applique à :** Windows | Serveur Windows_

## <a name="extensible-storage-engine"></a>Moteur de stockage extensible

Le moteur ESE (Extensible Storage Engine) est une technologie de stockage avancée d’index et de méthode d’accès séquentiel (ISAM). Le moteur ESE permet aux applications de stocker et de récupérer des données à partir de tables à l’aide de la navigation de curseurs indexée ou séquentielle. Il prend en charge les schémas dénormalisés, y compris les tables larges avec de nombreuses colonnes éparses, les colonnes à valeurs multiples et les index incomplets et enrichis. Elle permet aux applications de bénéficier d’un état de données cohérent à l’aide de la mise à jour et de la récupération des données transactionnelles. Un mécanisme de récupération après incident est fourni pour assurer la cohérence des données, même en cas de panne du système. Il fournit des transactions ACID (à durabilité isolée cohérente atomique) sur les données et le schéma au moyen d’un journal d’écriture anticipée et d’un modèle d’isolation d’instantané. Les transactions dans ESE sont hautement simultanées, ce qui rend le moteur ESE utile pour les applications serveur. Il met en cache les données pour optimiser l’accès aux données à hautes performances. En outre, il est léger, ce qui le rend utile pour les applications qui sont utilisées dans des rôles auxiliaires.

Le moteur ESE est destiné à être utilisé dans les applications qui nécessitent un stockage de données structuré rapide et/ou léger, où l’accès aux fichiers bruts ou le registre ne prend pas en charge l’indexation ou les exigences de taille de données de l’application.

Elle est utilisée par les applications qui ne stockent jamais plus de 1 méga-octets de données et qui ont été utilisées dans les applications avec des bases de données dans des cas extrêmes dépassant 1 téraoctet et généralement plus de 50 gigaoctets.

Cette documentation est destinée aux développeurs familiarisés avec C et C++, ainsi qu’à des concepts de base de données de base tels que les tables, les colonnes, les index, la récupération et les transactions. La seule méthode d’accès pour ESE est l’API C décrite dans cette documentation.

Le moteur de stockage extensible est un composant Windows qui a été introduit dans Windows 2000. Toutes les fonctionnalités ou les API ne sont pas disponibles dans toutes les versions des systèmes d’exploitation Windows.

ESE fournit un moteur de stockage en mode utilisateur qui gère des données à l’intérieur de fichiers binaires plats accessibles par le biais des API Windows. Le moteur ESE est accessible via une DLL qui est chargée directement dans le processus de l’application. aucune méthode d’accès à distance n’est requise ou fournie par le moteur de base de données lui-même. Bien que le moteur ESE n’ait pas de méthode d’accès distant ou inter-processus, les fichiers de données qu’il utilise peuvent être fournis à distance à l’aide du protocole SMB (Server Message Block) via les API Windows, mais cela n’est pas recommandé.

**Remarque**  Windows XP 64-bit Edition est le même que Windows Server 2003 pour déterminer le jeu de fonctionnalités ESE pris en charge.

### <a name="notes"></a>Notes

Le moteur ESE était auparavant connu sous le nom de technologie JET (articulation Engine Technology), et le terme « Jet Blue » ou « JET » est donc utilisé de manière interchangeable avec le terme ESE en dehors de cette documentation. Toutefois, il existe en fait deux implémentations entièrement distinctes de l’API JET, appelées Blue JET et JET Red. Le terme « JET » est souvent utilisé pour faire référence à JET Red, qui est le moteur de base de données utilisé avec l’accès Microsoft Office. Les deux implémentations JET sont complètement différentes, elles sont gérées séparément, possèdent un ensemble de fonctionnalités très différent et ne sont pas interchangeables. Dans la documentation ESE, « JET » fait référence à l’API ESE ou JET dans la mesure où ESE l’implémente. Toutes les références au Red JET sont toujours étiquetées de manière explicite « JET Red ».

### <a name="in-this-section"></a>Dans cette section

[Informations de référence sur le moteur de stockage extensible](./extensible-storage-engine-reference.md)
