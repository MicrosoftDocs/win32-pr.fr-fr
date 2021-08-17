---
title: Pilotes (Guide de programmation pour l’Windows 64 bits)
description: la version 64 bits de Windows est conçue pour permettre aux développeurs d’utiliser une base de code source unique pour leurs applications 32 bits et 64 bits. dans une large mesure, cela est également vrai pour les pilotes Windows 32 bits et 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- pilotes 64 bits Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cda928bbfc8c7f83e3aeac0bacbaea1e1a46214d9c0785d4675a3042b87fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132852"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Pilotes (Guide de programmation pour l’Windows 64 bits)

la version 64 bits de Windows est conçue pour permettre aux développeurs d’utiliser une base de code source unique pour leurs applications 32 bits et 64 bits. dans une large mesure, cela est également vrai pour les pilotes Windows 32 bits et 64 bits.

toutefois, les pilotes 32 bits ne peuvent pas s’exécuter sur des Windows 64 bits et doivent être portés. pour les applications en mode utilisateur, la Windows 64 bits comprend WOW64, ce qui permet aux applications de Windows 32 bits de s’exécuter (avec une perte de performances) sur les systèmes qui exécutent le Windows 64 bits. Il n’existe aucune couche de traduction équivalente pour les pilotes.

pour plus d’informations sur le portage des pilotes vers Windows 64 bits, consultez [problèmes liés à 64 bits](https://msdn.microsoft.com/library/aa489627.aspx) dans le Kit de pilotes Windows (WDK).

 

 




