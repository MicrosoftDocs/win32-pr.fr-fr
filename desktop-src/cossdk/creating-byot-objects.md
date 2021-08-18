---
description: Création d’objets BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Création d’objets BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128762"
---
# <a name="creating-byot-objects"></a>Création d’objets BYOT

Un nouvel objet BYOT crée des objets avec des transactions manuelles. Les deux interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) et [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), ont une méthode unique, **CreateInstance**, qui prend respectivement un pointeur d’interface **ITransaction** et une URL Tip. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) retourne un pointeur d’interface vers l’objet nouvellement créé, qui est inscrit dans la transaction spécifiée.

Lorsqu’un objet avec une transaction manuelle est publié, COM+ ne tente pas de valider la transaction. La transaction est contrôlée explicitement par le gestionnaire de transactions externe qui a distribué la transaction sous laquelle cet objet a été créé.

> [!Note]  
> L’objet BYOT. ByotServerEx doit être importé dans une application COM+.

 

 

 



