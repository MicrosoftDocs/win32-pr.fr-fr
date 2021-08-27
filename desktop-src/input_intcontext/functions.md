---
title: Fonctions de contexte d’interaction
description: Les rubriques de cette section fournissent les spécifications de référence pour les fonctions de contexte d’interaction.
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- intervention de l'utilisateur
- entrée
- pointeur
- interface tactile
- souris
- stylet
- stylet
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 5f0769aa5b9b097b23206c0515bd32552a59969404e72bbfcf26973d5d4f3de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758335"
---
# <a name="interaction-context-functions"></a>Fonctions de contexte d’interaction

Les rubriques de cette section fournissent les spécifications de référence pour les fonctions de [contexte d’interaction](interaction-context-portal.md) .

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Inclut le pointeur spécifié dans le jeu de pointeurs traités par l’objet de [contexte d’interaction](interaction-context-portal.md) . <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Ajoute l’historique d’un pointeur d’entrée unique à la mémoire tampon de l’objet de [contexte d’interaction](interaction-context-portal.md) .<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Crée et initialise un objet de [contexte d’interaction](interaction-context-portal.md) .<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Détruit l’objet de [contexte d’interaction](interaction-context-portal.md) spécifié.<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Obtient le comportement d’interaction entre les diapositives. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Obtient le comportement d’inertie d’une manipulation (translation, rotation, mise à l’échelle). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Obtient l’état de configuration de l’interaction pour l’objet de [contexte d’interaction](interaction-context-portal.md) .<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Obtient l’état de la roulette de la souris pour l’objet de [contexte d’interaction](interaction-context-portal.md) . <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Obtient les propriétés de l’objet de [contexte d’interaction](interaction-context-portal.md) .<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Obtient l’état du [contexte d’interaction](interaction-context-portal.md) actuel et l’heure à laquelle le contexte repasse à l’état inactif. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Traitez les paquets mis en mémoire tampon à la fin d’un frame d’entrée de pointeur.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Envoie l’entrée du minuteur à l’objet de [contexte d’interaction](interaction-context-portal.md) pour le traitement de l’inertie.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Traite un ensemble de frames d’entrée de pointeur.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Inscrit un rappel pour recevoir des événements d’interaction à partir d’un objet de [contexte d’interaction](interaction-context-portal.md) .<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Supprime le pointeur spécifié de l’ensemble de pointeurs traités par l’objet de [contexte d’interaction](interaction-context-portal.md) . <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Réinitialise l' [**État d’interaction**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state), les paramètres de configuration de l’interaction et tous les paramètres à leur état initial. Les interactions actuelles sont annulées sans notifications. <br/> Le [contexte d’interaction](interaction-context-portal.md) doit être reconfiguré avant l’utilisation suivante.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Configure l’interaction entre les diapositives. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Configure le comportement d’inertie d’une manipulation (translation, rotation, mise à l’échelle) après la levée du contact. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Configure l’objet de [contexte d’interaction](interaction-context-portal.md) pour traiter les manipulations spécifiées.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Définit les valeurs de paramètre pour l’entrée de la roulette de la souris. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Définit le point central et le rayon pivot à partir du point central, pour une manipulation de rotation à l’aide d’un pointeur d’entrée unique. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Définit les propriétés de l’objet de [contexte d’interaction](interaction-context-portal.md) .<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Définit l' [**État**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) d’interaction sur \_ État d’interaction \_ inactif et laisse tous les paramètres et paramètres de configuration d’interaction intacts. Les interactions actuelles sont annulées et les notifications sont envoyées en fonction des besoins.<br/> Il n’est pas nécessaire de reconfigurer le [contexte d’interaction](interaction-context-portal.md) avant l’utilisation suivante.<br/> |

## <a name="related-topics"></a>Rubriques connexes

[Référence du contexte d’interaction](interaction-context-reference.md)
