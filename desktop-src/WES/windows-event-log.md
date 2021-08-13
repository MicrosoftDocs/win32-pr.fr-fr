---
title: Journal des événements Windows
description: l’API du journal des événements Windows définit le schéma que vous utilisez pour écrire un manifeste d’instrumentation.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4306ce9722aba5b06109265c71cf387af2b35f63aef1cec070936400fff61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587194"
---
# <a name="windows-event-log"></a>Journal des événements Windows

## <a name="purpose"></a>Fonction

l’API du journal des événements Windows définit le schéma que vous utilisez pour écrire un manifeste d’instrumentation. Un manifeste d’instrumentation identifie votre fournisseur d’événements et les événements qu’il enregistre. L’API comprend également les fonctions qu’un consommateur d’événements, tel que le [Observateur d’événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), utiliserait pour lire et restituer les événements. Pour écrire les événements définis dans le manifeste, utilisez les fonctions incluses dans l’API de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW).

Windows le journal des événements remplace l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) en commençant par le système d’exploitation Windows Vista.

## <a name="developer-audience"></a>Développeurs concernés

Windows Le journal des événements est conçu pour les programmeurs C/C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

Windows le journal des événements est inclus dans le système d’exploitation à partir de Windows Vista et Windows Server 2008.

Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

Pour obtenir un historique complet des versions, consultez [Nouveautés](what-s-new.md).

## <a name="in-this-section"></a>Contenu de cette section


| Rubrique                                                        | Description                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [utilisation du journal des événements Windows](using-windows-event-log.md)        | guide procédural qui montre comment utiliser l’API du journal des événements Windows.                                 |
| [Windows Référence du journal des événements](windows-event-log-reference.md)| Les types de données, les fonctions, les énumérations, les structures, les constantes et les schémas inclus dans l’API.|