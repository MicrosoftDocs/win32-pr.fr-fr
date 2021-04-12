---
title: Position
description: Une composition est un état d’entrée temporaire qui permet à un service de texte de spécifier à la fois à l’application et à l’utilisateur que le texte d’entrée est toujours dans un état de modification.
ms.assetid: 3d9da4f2-ceb9-4abc-8979-d3756d948a57
keywords:
- Text Services Framework (TSF), compositions
- TSF (Text Services Framework), compositions
- services de texte, compositions
- Applications compatibles TSF, compositions
- compositions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b03f3e991f76ee7c6dca3830267796576c7b842
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382430"
---
# <a name="compositions"></a>Position

Une composition est un état d’entrée temporaire qui permet à un service de texte de spécifier à la fois à l’application et à l’utilisateur que le texte d’entrée est toujours dans un état de modification. Une application peut et doit obtenir des informations sur les attributs d’affichage sur la composition et utiliser ces informations pour afficher l’état de la composition à l’utilisateur.

Un exemple de l’utilisation d’une composition est l’entrée vocale. Pendant que l’utilisateur parle, le service de texte vocal crée une composition. Cette composition reste intacte jusqu’à ce que toute la saisie vocale soit terminée. À la fin de la session, le service de texte vocal met fin à la composition.

Une application utilise la présence et l’absence d’une composition pour déterminer comment afficher du texte et ce qui, le cas échéant, le traitement doit être effectué sur le texte. Par exemple, si l’utilisateur utilise le moteur de reconnaissance vocale pour entrer du texte, l’application ne doit effectuer aucune vérification orthographique ou grammaticale sur un texte de composition. Le texte est considéré comme incomplet jusqu’à la fin de la composition.

## <a name="text-services"></a>Services de texte

Un service de texte crée une composition en appelant [ITfContextComposition :: StartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextcomposition-startcomposition). Le service de texte peut éventuellement implémenter un objet [ITfCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcompositionsink) qui reçoit des notifications d’événements de composition. StartComposition retourne un objet [ITfComposition](/windows/desktop/api/msctf/nn-msctf-itfcomposition) auquel le service de texte conserve une référence et utilise pour modifier et terminer la composition. Le service de texte met fin à la composition en appelant [ITfComposition :: EndComposition](/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition).

Si un service de texte va créer des compositions, il doit également prendre en charge les attributs d’affichage pour permettre à une application d’afficher du texte qui fait partie d’une composition différente du texte standard. Pour plus d’informations, consultez [fourniture d’attributs d’affichage](providing-display-attributes.md).

## <a name="applications"></a>Applications

Une application peut surveiller la création, la modification et l’arrêt des compositions en installant un récepteur [ITfContextOwnerCompositionSink](/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink) . Quand une composition est démarrée, [ITfContextOwnerCompositionSink :: OnStartComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition) est appelée. De même, lorsqu’une composition est modifiée ou terminée, [ITfContextOwnerCompositionSink :: OnUpdateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onupdatecomposition) et [ITfContextOwnerCompositionSink :: OnEndComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition) sont appelés, respectivement.

Voici une procédure classique pour mettre à jour un document à l’aide d’une composition.

1.  [ITextStoreACP :: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection) ou [ITextStoreAnchor :: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection) sont généralement utilisés pour insérer le texte initial dans la composition.
2.  La composition est démarrée avec un appel à [ITfContextComposition :: StartComposition](/windows/desktop/api/Msctf/nf-msctf-itfcontextcomposition-startcomposition), à l’aide de la plage de texte retournée par **InsertTextAtSelection**.
3.  Lorsqu’il reçoit une nouvelle entrée telle qu’une entrée vocale ou clavier, l’application met à jour la composition avec [ITextStoreACP :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext) ou [ITextStoreAnchor :: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext).
4.  Lorsque l’application détermine qu’il est temps de mettre fin à la composition, elle appelle [ITfComposition :: EndComposition](/windows/desktop/api/Msctf/nf-msctf-itfcomposition-endcomposition).

L’application doit utiliser les attributs d’affichage fournis par le service de texte pour modifier l’affichage du texte à tout moment, et pas seulement quand une composition est active. Pour plus d’informations, consultez [utilisation des attributs d’affichage](using-display-attributes.md).

Si nécessaire, une application peut arrêter une composition en appelant [ITfContextOwnerCompositionServices :: TerminateComposition](/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionservices-terminatecomposition).

 

 