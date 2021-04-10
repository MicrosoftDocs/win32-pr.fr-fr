---
title: Développement d’un fournisseur
description: Pour écrire les événements que vous définissez dans votre manifeste, vous utilisez les fonctions incluses dans l’API de suivi d’événements (ETW). Pour plus d’informations sur l’écriture d’un fournisseur, consultez fourniture d’événements.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102205"
---
# <a name="developing-a-provider"></a>Développement d’un fournisseur

Pour écrire les événements que vous définissez dans votre manifeste, vous utilisez les fonctions incluses dans l’API de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW). Pour plus d’informations sur l’écriture d’un fournisseur, consultez [fourniture d’événements](/windows/desktop/ETW/providing-events).

Après avoir écrit le fournisseur, utilisez l’outil WevtUtil.exe pour inscrire le fournisseur et le schéma. Pour plus d’informations sur l’utilisation de WevtUtil, consultez [outils du journal des événements Windows](windows-event-log-tools.md). L’exemple suivant montre comment utiliser WevtUtil pour inscrire un fournisseur et supprimer l’inscription.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```