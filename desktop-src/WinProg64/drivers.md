---
title: Pilotes (Guide de programmation pour Windows 64 bits)
description: La version 64 bits de Windows est conçue pour permettre aux développeurs d’utiliser une base de code source unique pour leurs applications 32 bits et 64 bits. Dans une large mesure, cela est également vrai pour les pilotes Windows 32 bits et 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- pilotes de programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317061"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Pilotes (Guide de programmation pour Windows 64 bits)

La version 64 bits de Windows est conçue pour permettre aux développeurs d’utiliser une base de code source unique pour leurs applications 32 bits et 64 bits. Dans une large mesure, cela est également vrai pour les pilotes Windows 32 bits et 64 bits.

Toutefois, les pilotes 32 bits ne peuvent pas s’exécuter sous Windows 64 bits et doivent être portés. Pour les applications en mode utilisateur, Windows 64 bits comprend WOW64, ce qui permet aux applications Windows 32 bits de s’exécuter (avec une perte de performances) sur les systèmes qui exécutent Windows 64 bits. Il n’existe aucune couche de traduction équivalente pour les pilotes.

Pour plus d’informations sur le portage des pilotes vers Windows 64 bits, consultez [problèmes liés à 64 bits](https://msdn.microsoft.com/library/aa489627.aspx) dans le kit de pilotes Windows (WDK).

 

 




