---
title: L’environnement
description: Les développeurs qui travaillent sur des applications pour Windows 64 bits trouveront l’environnement de développement quasiment identique à l’environnement de développement pour Windows 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- environnement de développement 64 programmation Windows bits
- environnement de programmation Windows 64 bits
- Guide de programmation Windows 64 bits sur la programmation Windows 64 bits, environnement de développement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104ea1bdacbb478eaa0abcf46d04c3d772540f26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028879"
---
# <a name="the-environment"></a>L’environnement

Les développeurs qui travaillent sur des applications pour Windows 64 bits trouveront l’environnement de développement quasiment identique à l’environnement de développement pour Windows 32 bits. Les API existantes ont été modifiées, le cas échéant, afin de leur permettre de refléter la précision de la plateforme sur laquelle elles s’exécutent. Le résultat est la simplicité et une petite courbe d’apprentissage pour le développeur : écrire du code pour Windows 64 bits revient à écrire du code pour Windows 32 bits.

Les fichiers d’en-tête Windows prennent en charge de nouveaux types de données qui permettent aux pointeurs et aux variables associées au pointeur de refléter la précision de la plateforme. Cela signifie que les développeurs peuvent compiler une base source unique pour une exécution en mode natif sur Windows 32 bits ou Windows 64 bits. Cette stratégie réduit le coût du développement d’applications qui tirent parti du matériel 64, comme les processeurs AMD Opteron ou Athlon64 ou les processeurs Intel Itanium.

Vous aurez plus de temps pour rendre vos applications 64 bits prêtes si vous adoptez les nouvelles conventions de type de données dès que possible. Si vous modifiez votre code, vous devez modifier les définitions de données en même temps. Testez l’application sur Windows 32 bits, exécutez-la via le compilateur 64 bits (décrit dans [les outils](the-tools.md)) et l’application sera prête à être testée lorsque vous disposerez du matériel 64 bits approprié.

 

 




