---
title: Synchronisation des rappels
description: Synchronisation des rappels
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f85f388a81b6568db502b4f9843cc7fb9135bfaa9f3529a301993aeac87c43c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859639"
---
# <a name="callback-synchronization"></a>Synchronisation des rappels

L' [API WinInet](/windows/desktop/WinInet/portal) asynchrone (utilisée pour les protocoles les plus courants) laisse la synchronisation du mécanisme de rappel et de l’application appelante en tant qu’exercice pour le client. Cette opération est intentionnelle car elle offre le plus grand degré de flexibilité. Les protocoles par défaut et l’implémentation du moniker d’URL effectuent cette synchronisation et garantissent que les applications à thread unique et à thread cloisonné n’ont jamais à gérer la contention de style thread libre. Autrement dit, les interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) et [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) du client sont appelées uniquement sur leurs threads appropriés. Cette fonctionnalité est transparente pour l’utilisateur de l’URL mMoniker tant que chaque thread qui appelle [**IMoniker :: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) et [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) a une file d’attente de messages.

La spécification du moniker asynchrone requiert un contrôle plus précis de la définition des priorités et de la gestion des téléchargements que ce qui est autorisé par WinSock ou WinInet. En conséquence, un moniker d’URL gère tous les téléchargements pour tout thread appelant donné, en utilisant (dans le cadre de sa synchronisation) un schéma de priorité basé sur la spécification [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Monikers d’URL](url-monikers.md)
</dt> </dl>

 

 