---
title: L’environnement
description: les développeurs qui travaillent sur des applications pour la Windows 64 bits trouveront l’environnement de développement quasiment identique à l’environnement de développement pour les Windows 32 bits.
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- programmation Windows de l’environnement de développement 64 bits
- environnement 64-Windows bits (programmation)
- guide de programmation Windows 64 bits 64-bits Windows programmation, environnement de développement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69580d6537c832abaf51b20a553c4e4e788a6013bdfc14a8002f60de9872da62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734129"
---
# <a name="the-environment"></a>L’environnement

les développeurs qui travaillent sur des applications pour la Windows 64 bits trouveront l’environnement de développement quasiment identique à l’environnement de développement pour les Windows 32 bits. Les API existantes ont été modifiées, le cas échéant, afin de leur permettre de refléter la précision de la plateforme sur laquelle elles s’exécutent. le résultat est la simplicité et une petite courbe d’apprentissage pour le développeur : l’écriture de code pour l’Windows de 64 bits est semblable à l’écriture de code pour les Windows 32 bits.

les fichiers d’en-tête Windows prennent en charge de nouveaux types de données qui permettent aux pointeurs et aux variables associées au pointeur de refléter la précision de la plateforme. cela signifie que les développeurs peuvent compiler une seule base source pour qu’elle s’exécute en mode natif sur les Windows 32 bits ou sur 64 bits Windows. Cette stratégie réduit le coût du développement d’applications qui tirent parti du matériel 64, comme les processeurs AMD Opteron ou Athlon64 ou les processeurs Intel Itanium.

Vous aurez plus de temps pour rendre vos applications 64 bits prêtes si vous adoptez les nouvelles conventions de type de données dès que possible. Si vous modifiez votre code, vous devez modifier les définitions de données en même temps. testez l’application sur l’Windows 32 bits, exécutez-la par le biais du compilateur 64 bits (décrit dans [les outils](the-tools.md)) et l’application sera prête à être testée lorsque vous disposerez du matériel 64 bits approprié.

 

 




