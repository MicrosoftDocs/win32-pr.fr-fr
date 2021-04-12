---
description: Au fil du temps, différentes versions de TAPI, d’applications et de fournisseurs de services peuvent être générées.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Contrôle de version TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319690"
---
# <a name="tapi-versioning"></a>Contrôle de version TAPI

Au fil du temps, différentes versions de TAPI, d’applications et de fournisseurs de services peuvent être générées. Ces nouvelles versions peuvent créer de nouvelles définitions, telles que des nouvelles fonctionnalités, de nouveaux membres dans les structures de données et de nouveaux champs de bits. Les numéros de version sont donc nécessaires pour indiquer comment interpréter diverses structures de données.

Pour permettre une interopérabilité optimale des différentes versions des applications, des versions de l’interface TAPI elle-même et des versions des fournisseurs de services par différents fournisseurs, Microsoft Telephony fournit un mécanisme de négociation de version simple pour les applications. Il existe deux versions différentes que TAPI et le fournisseur de services de téléphonie doivent accepter pour chaque périphérique de ligne. La première est la version négociée avec TAPI et le fournisseur de services de téléphonie (TSP) de base et la téléphonie supplémentaire, appelée « version de l’interface TAPI ». L’autre est pour les extensions spécifiques au fournisseur, le cas échéant, et est appelée version de l’extension. Le format des structures de données et des types de données utilisés par les fonctionnalités de base et supplémentaires de l’interface TAPI est défini par la version TAPI, tandis que la version d’extension détermine le format des structures de données définies par les extensions spécifiques au fournisseur.

La fonction [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) négocie une version TAPI et [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) négocie la version de l’extension TSP. Un seul TSP peut être capable de gérer plusieurs versions, et une application doit « revenir » à l’utilisation d’une version antérieure si vous utilisez un TSP plus ancien. Dans **lineNegotiateAPIVersion** , le paramètre *dwApiVersion* a une valeur par défaut en fonction de la version, comme suit.



| Version TAPI | Valeur par défaut |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

Toutefois, TAPI est beaucoup plus facile tant que le TSP lui-même utilise une version plus récente que celle de l’application. Si le TSP est effectivement plus récent, TAPI peut alors traduire « en baisse » vers la version de l’application. Par exemple, TAPI 2,0 TSPs n’a pas besoin d’être spécifiquement en charge de la gestion de TAPI version 1,4. Si une application TAPI 1,4 est exécutée, TAPI convertit tous les messages et structures TAPI 2,0 en équivalents TAPI 1,4, ou aussi près que possible. S’il n’existe aucune approximation proche dans TAPI 1,4, toutes les informations spécifiques à TAPI 2,0 seront perdues.

La signification précise d’une version d’extension est spécifique au fournisseur. Pour utiliser un TSP qui prend en charge les extensions, consultez la documentation du fournisseur.

Il existe plusieurs versions de TAPI. Alors que la plupart de ces versions impliquaient des modifications dans les ensembles de documentation TAPI et TSPI (Telephony Service Provider Interface), il existe d’autres implications pour chaque version, à savoir, les différences architecturales, les variantes du système d’exploitation, les redistribuables et les problèmes de développement TSP.



| Version TAPI        | Distribution                                                   |
|---------------------|----------------------------------------------------------------|
| 1,0 – 1,2           | Versions bêta qui ne doivent plus être utilisées.              |
| [1.4](tapi-1-4.md) | Inclus dans Windows 95.                                        |
| [1.5](tapi-1-5.md) | Inclus dans Windows CE 1,0.                                    |
| [2.0](tapi-2-0.md) | Inclus dans Windows NT 4,0 avec SP3.                           |
| [2.1](tapi-2-1.md) | Inclus dans Windows NT 4,0 avec SP4 et Windows 98.            |
| [2.2](tapi-2-2.md) | Inclus dans Windows Server 2003, Windows XP et Windows 2000. |



 

 

 



