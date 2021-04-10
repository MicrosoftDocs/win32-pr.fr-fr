---
title: Journal des événements Windows
description: L’API du journal des événements Windows définit le schéma que vous utilisez pour écrire un manifeste d’instrumentation.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842706"
---
# <a name="windows-event-log"></a>Journal des événements Windows

## <a name="purpose"></a>Objectif

L’API du journal des événements Windows définit le schéma que vous utilisez pour écrire un manifeste d’instrumentation. Un manifeste d’instrumentation identifie votre fournisseur d’événements et les événements qu’il enregistre. L’API comprend également les fonctions qu’un consommateur d’événements, tel que le [Observateur d’événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), utiliserait pour lire et restituer les événements. Pour écrire les événements définis dans le manifeste, utilisez les fonctions incluses dans l’API de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW).

Le journal des événements Windows remplace l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) en commençant par le système d’exploitation Windows Vista.

## <a name="developer-audience"></a>Développeurs concernés

Le journal des événements Windows est conçu pour les programmeurs C/C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

Le journal des événements Windows est inclus dans le système d’exploitation à compter de Windows Vista et de Windows Server 2008.

Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

Pour obtenir un historique complet des versions, consultez [Nouveautés](what-s-new.md).

## <a name="in-this-section"></a>Contenu de cette section


| Rubrique                                                        | Description                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Utilisation du journal des événements Windows](using-windows-event-log.md)        | Guide procédural qui montre comment utiliser l’API du journal des événements Windows.                                 |
| [Informations de référence sur le journal des événements Windows](windows-event-log-reference.md)| Les types de données, les fonctions, les énumérations, les structures, les constantes et les schémas inclus dans l’API.|