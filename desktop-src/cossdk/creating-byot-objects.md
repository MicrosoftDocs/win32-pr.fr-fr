---
description: Création d’objets BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Création d’objets BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514529"
---
# <a name="creating-byot-objects"></a>Création d’objets BYOT

Un nouvel objet BYOT crée des objets avec des transactions manuelles. Les deux interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) et [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), ont une méthode unique, **CreateInstance**, qui prend respectivement un pointeur d’interface **ITransaction** et une URL Tip. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) retourne un pointeur d’interface vers l’objet nouvellement créé, qui est inscrit dans la transaction spécifiée.

Lorsqu’un objet avec une transaction manuelle est publié, COM+ ne tente pas de valider la transaction. La transaction est contrôlée explicitement par le gestionnaire de transactions externe qui a distribué la transaction sous laquelle cet objet a été créé.

> [!Note]  
> L’objet BYOT. ByotServerEx doit être importé dans une application COM+.

 

 

 



