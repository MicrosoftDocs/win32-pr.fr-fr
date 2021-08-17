---
title: Développement d’un fournisseur
description: Pour écrire les événements que vous définissez dans votre manifeste, vous utilisez les fonctions incluses dans l’API de suivi d’événements (ETW). Pour plus d’informations sur l’écriture d’un fournisseur, consultez fourniture d’événements.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937184"
---
# <a name="developing-a-provider"></a>Développement d’un fournisseur

Pour écrire les événements que vous définissez dans votre manifeste, vous utilisez les fonctions incluses dans l’API de [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW). Pour plus d’informations sur l’écriture d’un fournisseur, consultez [fourniture d’événements](/windows/desktop/ETW/providing-events).

Après avoir écrit le fournisseur, utilisez l’outil WevtUtil.exe pour inscrire le fournisseur et le schéma. pour plus d’informations sur l’utilisation de WevtUtil, consultez [Windows les outils du journal des événements](windows-event-log-tools.md). L’exemple suivant montre comment utiliser WevtUtil pour inscrire un fournisseur et supprimer l’inscription.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```