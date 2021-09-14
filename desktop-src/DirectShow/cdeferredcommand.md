---
description: Les commandes différées sont mises en file d’attente par des appels à des méthodes sur l’interface IQueueCommand et sont exposées par le gestionnaire de graphique de filtre et par certains filtres.
ms.assetid: b2b177c6-af2b-4585-914f-001a6355a298
title: CDeferredCommand, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8d3db3f35b5589a6cd17791d72aa9931124ccfbb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007642"
---
# <a name="cdeferredcommand-class"></a>CDeferredCommand, classe

![hiérarchie de la classe cdeferredcommand](images/cutil13.png)

Les commandes différées sont mises en file d’attente par des appels à des méthodes sur l’interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) et sont exposées par le gestionnaire de graphique de filtre et par certains filtres. Un appel réussi à l’une de ces méthodes retourne une interface [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) représentant la commande mise en file d’attente.

Un `CDeferredCommand` objet représente une commande différée unique et expose l’interface [**IDeferredCommand**](/windows/desktop/api/Control/nn-control-ideferredcommand) ainsi que d’autres méthodes qui autorisent les contrôles de temps et l’exécution réelle. Un `CDeferredCommand` objet contient une référence à l’objet [**CCmdQueue**](ccmdqueue.md) sur lequel il est mis en file d’attente.

Les décomptes de références contrôlent la durée de vie de la `CDeferredCommand` classe. Lors de l’appel de la fonction membre [**CDeferredCommand :: Invoke**](cdeferredcommand-invoke.md) , l’application appelante obtient un pointeur d’interface qui fait l’objet d’un comptage des références, et l’objet [**CCmdQueue**](ccmdqueue.md) contient également un décompte de références sur la commande différée. L’appel de la fonction membre [**IDeferredCommand :: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) prend la commande différée de la file d’attente de commandes et réduit ainsi le nombre de références d’une unité. Une fois que vous avez retiré la file d’attente, la commande ne peut pas être replacée dans la file d’attente.



| Membres de données protégés                                        | Description                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| m \_ bStream                                                    | Indicateur de temps de [**flux**](stream-time.md) ou d’heure de présentation. à passer à la méthode appelée.                   |
| m \_ Dispatch                                                   | Accède à l’interface **ITypeInfo** .                                                                                   |
| m \_ dispidMethod                                               | Méthode sur l’interface à exécuter.                                                                                         |
| m \_ DispParams                                                 | Objet [**CDispParams**](cdispparams.md) contenant la liste de paramètres **DISPPARAMS**                                  |
| m \_ hrResult                                                   | Stocke la valeur **HRESULT** retournée.                                                                                  |
| m \_ IID                                                        | Identificateur global unique (**GUID**) de l’interface.                                                                 |
| m \_ pQueue                                                     | Pointeur vers l’objet [**CCmdQueue**](ccmdqueue.md) qui expose l’interface [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) . |
| m \_ punk                                                       | Pointeur **IUnknown** vers l’interface sur laquelle la commande sera exécutée.                                                 |
| m \_ pvarResult                                                 | Les informations résultantes, le cas échéant, de la méthode appelée.                                                                 |
| m \_ heure                                                       | Heure à laquelle la commande sera exécutée.                                                                                  |
| m \_ wFlags                                                     | Indicateurs spécifiant le contexte de l’appel.                                                                         |
| Fonctions de membre                                              | Description                                                                                                             |
| [**CDeferredCommand**](cdeferredcommand-cdeferredcommand.md) | Construit un objet **CDeferredCommand** .                                                                               |
| [**GetFlags**](cdeferredcommand-getflags.md)                 | Récupère les indicateurs de contexte associés à la commande différée.                                                       |
| [**GetIID**](cdeferredcommand-getiid.md)                     | Récupère l’identificateur d’interface (IID) de l’interface sur laquelle la méthode sera exécutée.                              |
| [**GetMethod,**](cdeferredcommand-getmethod.md)               | Récupère l’identificateur de dispatch de la méthode à exécuter.                                                              |
| [**GetParams**](cdeferredcommand-getparams.md)               | Récupère la liste d’arguments **DISPPARAMS** à la méthode.                                                               |
| [**GetResult**](cdeferredcommand-getresult.md)               | Récupère la liste d’arguments résultante, le cas échéant.                                                                   |
| [**GetTime**](cdeferredcommand-gettime.md)                   | Récupère l’heure à laquelle la méthode sera exécutée.                                                                         |
| [**Appeler**](cdeferredcommand-invoke.md)                     | Fournit l’accès aux méthodes et propriétés exposées par un objet.                                                         |
| [**IsStreamTime**](cdeferredcommand-isstreamtime.md)         | Spécifie si la commande doit être exécutée au moment du flux ou de la présentation.                                         |
| Méthodes IDeferredCommand                                      | Description                                                                                                             |
| [**Annuler**](cdeferredcommand-cancel.md)                     | Annule une demande [**CDeferredCommand :: Invoke**](cdeferredcommand-invoke.md) précédemment mise en file d’attente.                        |
| [**Garantir**](cdeferredcommand-confidence.md)             | Actuellement non implémenté.                                                                                              |
| [**Reporter**](cdeferredcommand-postpone.md)                 | Spécifie une nouvelle heure de présentation pour une commande précédemment mise en file d’attente.                                                      |
| [**GetHRESULT,**](cdeferredcommand-gethresult.md)             | Récupère la valeur **HRESULT** de la méthode appelée.                                                                  |



 

 

 



