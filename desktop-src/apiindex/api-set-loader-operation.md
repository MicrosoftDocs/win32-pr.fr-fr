---
description: Décrit comment Windows 10 utilise des ensembles d’API dans les opérations du chargeur.
title: Opération du chargeur de l’ensemble d’API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 701409c0d8dac2c275add06d2502c8764d502aba
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "106525776"
---
# <a name="api-set-loader-operation"></a>Opération du chargeur de l’ensemble d’API

Les [ensembles d’API](windows-apisets.md) s’appuient sur la prise en charge du système d’exploitation dans le chargeur de bibliothèque pour introduire efficacement une redirection d’espace de noms de module dans le processus de liaison de bibliothèque. Le [nom de contrat](windows-apisets.md#api-set-contract-names) de l’ensemble d’API est utilisé par le chargeur de bibliothèque pour effectuer une redirection du runtime de la référence à un fichier binaire hôte cible qui héberge l’implémentation appropriée de l’ensemble d’API.

Lorsque le chargeur rencontre une dépendance sur un ensemble d’API au moment de l’exécution, le chargeur consulte les données de configuration dans l’image pour identifier le binaire de l’hôte pour un ensemble d’API. Ces données de configuration sont appelées le schéma de l' **ensemble d’API**. Le schéma est assemblé en tant que propriété du système d’exploitation, et le mappage entre les jeux d’API et les binaires peut varier en fonction des fichiers binaires inclus dans un appareil donné. Le schéma permet de router correctement une fonction importée dans un fichier binaire unique sur différents appareils, même si les noms des modules de l’hôte binaire ont été renommés ou complètement refactorisés sur des appareils Windows différents.

Windows 10 prend en charge deux techniques standard pour consommer et interagir avec les ensembles d’API : le **transfert direct** et le **transfert inverse**.

### <a name="direct-forwarding"></a>Transfert direct

Dans cette configuration, le code de consommation importe directement un nom de module d’ensemble d’API. Cette importation est résolue en une seule opération et constitue la méthode la plus efficace avec la surcharge la plus faible. D’un point de vue conceptuel, cette solution peut pointer vers différents binaires sur différents appareils Windows 10, comme indiqué dans l’exemple suivant :

Ensemble d’API importé : **api-feature1-l1-1-0.dll**
-  PC Windows-> **feature1.dll**
-  HoloLens-> **feature1_holo.dll**
-  IoT-> **feature1_iot.dll**

Étant donné que les mappages sont conservés dans un référentiel de données de schéma personnalisé, cela signifie qu’un nom d’ensemble d’API qui se termine par **. dll** ne fait pas directement référence à un fichier sur le disque. La partie **. dll** du nom de l’ensemble d’API est uniquement une convention requise par le chargeur. Le nom de l’ensemble d’API est plus similaire à un alias ou un nom virtuel pour un fichier DLL physique. Cela rend le nom portable sur la totalité de la plage d’appareils Windows 10.

### <a name="reverse-forwarding"></a>Transfert inversé

Bien que les noms des ensembles d’API fournissent un espace de noms stable pour les modules sur plusieurs appareils, il n’est pas toujours pratique de convertir chaque binaire en ce nouveau système. Par exemple, une application peut avoir été couramment utilisée depuis de nombreuses années, et la recompilation des binaires de l’application peut ne pas être possible. En outre, il se peut que certaines applications doivent continuer à s’exécuter sur des systèmes générés avant l’introduction de jeux d’API spécifiques.

Pour prendre en charge ce niveau de compatibilité, un système de *redirecteurs* est fourni sur tous les appareils Windows 10 qui couvrent un sous-ensemble de la surface de l’API Win32. Ces redirecteurs utilisent les noms des modules qui ont été introduits sur les PC Windows et exploitent le système d’ensemble d’API pour assurer la compatibilité sur tous les appareils Windows 10.

L’opération de chargeur se comporte comme suit :

1.  Sur un appareil autre qu’un PC Windows, le chargeur affiche une dépendance de nom de module Windows PC héritée qui n’est pas présente sur l’appareil.
2.  Le chargeur localise un redirecteur d’ensemble d’API pour ce module et le charge en mémoire.
3.  Le redirecteur a un mappage pour l’API définie pour la fonction donnée appelée.
4.  Le chargeur trouve le fichier binaire d’hôte approprié pour l’appareil donné.

D’un plan conceptuel, le mappage ressemble à ceci :

DLL importée : **feature1.dll**
- PC Windows-> **feature1.dll**
- HoloLens-> **feature1.dll** redirecteur-> **api-feature1-l1-1-0.dll**  ->  **feature1_holo.dll**
- Redirecteur IOT-> **feature1.dll** > **api-feature1-l1-1-0.dll**  ->  **feature1_iot.dll**

Le résultat final est le même que le [transfert direct](#direct-forwarding), mais il le remplit d’une manière qui optimise la compatibilité des applications.

> [!NOTE]
> Le transfert inverse fournit une couverture uniquement pour un sous-ensemble de la surface de l’API Win32. Elle n’autorise pas les applications qui ciblent les versions de bureau de Windows 10 à s’exécuter sur tous les appareils Windows 10.
