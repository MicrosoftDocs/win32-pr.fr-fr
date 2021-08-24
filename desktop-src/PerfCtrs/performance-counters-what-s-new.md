---
description: Cette section décrit les nouvelles fonctionnalités qui ont été ajoutées aux compteurs de performance pour chaque version.
ms.assetid: 14bdae6c-9dcd-401e-8c43-5391e00cf7e3
title: Nouveautés (compteurs de performances)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2c86a6a9ea644f1c650137cc392a2d54b6e8eedb34881d6b759d7b6c51635d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674699"
---
# <a name="whats-new-with-performance-counters"></a>Nouveautés des compteurs de performances

Cette section décrit les nouvelles fonctionnalités qui ont été ajoutées aux compteurs de performance pour chaque version.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 et Windows Server 2008 R2

L’outil [CTRPP](ctrpp.md) a été modifié pour améliorer et simplifier la génération de code. L’outil génère désormais uniquement un fichier d’en-tête et un fichier de ressources. Si vous souhaitez un ancien comportement de génération de code (non recommandé), vous pouvez utiliser le nouvel `-legacy` argument.

- Vous devez maintenant spécifier les nouveaux `-o` `-rc` arguments et qui spécifient respectivement le nom et l’emplacement de l’en-tête et du fichier de ressources.
- Vous pouvez utiliser l’argument New facultatif `-prefix` pour spécifier une chaîne à ajouter au début des variables globales et des fonctions définies dans le fichier d’en-tête généré.
- Si vous devez mettre à jour votre manifeste de compteurs, l’utilisation de la nouvelle génération de code élimine la nécessité de fusionner votre implémentation de rappel précédente avec le nouveau code généré, car les rappels ne sont plus inclus dans le code généré.

Un nouvel `symbol` attribut est disponible pour les éléments de manifeste suivants :

- [moteur](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
- [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element)
- [)](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element)

L' `symbol` attribut est requis pour [Provider](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) et [counterSet](/windows/desktop/PerfCtrs/performance-counters-counterset--provider--element), et est facultatif pour [Counter](/windows/desktop/PerfCtrs/performance-counters-counter--counterset--element). L’attribut vous permet de fournir un nom symbolique que vous pouvez utiliser pour référencer chaque élément lors de l’appel des fonctions du fournisseur (par exemple, vous pouvez utiliser le nom symbolique de l’ensemble de compteurs lors de l’appel de [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)).

## <a name="windows-vista"></a>Windows Vista

L’architecture des compteurs de performance pour la fourniture de données de compteur a été complètement modifiée pour cette version.

Précédemment, vous avez utilisé un fichier INI pour définir vos données de compteur et vous avez implémenté une DLL de performance qui a été exécutée dans le processus du consommateur pour fournir les données lorsqu’un consommateur l’a demandée. Cette architecture est déconseillée et n’est pas recommandée pour le nouveau code en raison de problèmes importants en matière de performances et de fiabilité.

La nouvelle architecture utilise un manifeste pour définir les données de compteur et exécute le code dans le processus du fournisseur pour fournir les données lorsqu’un consommateur le demande. Pour plus d’informations, consultez [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md).

Les fonctions suivantes ont été ajoutées pour cette version :

- [ControlCallback](/windows/desktop/api/Perflib/nc-perflib-perflibrequest)
- [PerfCreateInstance](/windows/desktop/api/Perflib/nf-perflib-perfcreateinstance)
- [PerfDeleteInstance](/windows/desktop/api/Perflib/nf-perflib-perfdeleteinstance)
- [PerfQueryInstance](/windows/desktop/api/Perflib/nf-perflib-perfqueryinstance)
- [PerfSetCounterSetInfo](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)
- [PerfSetULongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue)
- [PerfSetULongLongCounterValue](/windows/desktop/api/Perflib/nf-perflib-perfsetulonglongcountervalue)
- [PerfSetCounterRefValue](/windows/desktop/api/Perflib/nf-perflib-perfsetcounterrefvalue)
- [PerfStartProvider](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider)
- [PerfStopProvider](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider)

Les structures suivantes ont été ajoutées pour cette version :

- [\_identité du compteur de performances \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [\_informations sur le compteur de performances \_](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [\_informations du COUNTERSET de performance \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [\_instance du COUNTERSET de performance \_](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)

Pour obtenir la liste des éléments XML que vous utilisez dans votre manifeste pour définir vos compteurs, consultez [schéma des compteurs de performances](performance-counters-schema.md).

Pour plus d’informations sur l’outil de pré-processeur CTRPP qui analyse votre manifeste et génère le code que vous utilisez comme point de départ pour votre fournisseur, consultez [CTRPP](ctrpp.md).
