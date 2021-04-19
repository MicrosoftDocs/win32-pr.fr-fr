---
title: Développer des applications plateforme Windows universelle (UWP)
description: Développer des applications plateforme Windows universelle (UWP)
ms.assetid: 215256D7-CBBA-43B0-A99C-490A25D1F82C
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3654c1c8773a813fcc7f88b21a86c2ef6049184
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "106538993"
---
# <a name="develop-universal-windows-platform-uwp-apps"></a>Développer des applications plateforme Windows universelle (UWP)

Nous encourageons tous les éditeurs de logiciels indépendants (ISV) de l’application de bureau (Win32) à mettre vos applications de bureau à la [plateforme Windows universelle (UWP)](https://developer.microsoft.com/windows/bridges/desktop/) via le pont de bureau. Comme les applications UWP sont également prises en charge dans le [Windows Store](https://blogs.windows.com/buildingapps/2016/02/04/windows-store-trends-february-2016/), il vous est plus facile de mettre à jour automatiquement les applications de vos utilisateurs vers une version cohérente, ce qui réduit vos coûts de support technique.

Si vos applications de bureau ne peuvent pas être converties à l’aide du pont Desktop Bridge, nous vous recommandons vivement d’utiliser un programme d’installation qui suit les meilleures pratiques et de vérifier que cela est entièrement testé. Un programme d’installation est la première expérience de votre utilisateur ou de votre client avec votre application. Il arrive trop souvent qu’il ne fonctionne pas correctement ou qu’il n’a pas été complètement testé pour tous les scénarios. Le [Kit de certification des applications Windows](https://dev.windows.com/develop/app-certification-kit) peut vous aider à tester l’installation et la désinstallation de votre application Win32 et vous aider à identifier l’utilisation des API non documentées, ainsi que d’autres problèmes de base liés aux performances avant les utilisateurs.

## <a name="best-practices"></a>Meilleure pratique :

-   Utilisez des programmes d’installation qui fonctionnent à la fois pour les versions 32 bits et 64 bits de Windows.
-   Concevez vos programmes d’installation pour qu’ils fonctionnent dans plusieurs scénarios (niveau de l’utilisateur ou de l’ordinateur).
-   Conservez tous les composants redistribuables de Windows dans le package d’origine. Si vous réorganisez le package de ces composants, il se peut que le programme d’installation ne fonctionne pas correctement.
-   Planifiez le temps de développement de vos programmes d’installation ; ils sont souvent négligés en tant que livrables au cours du cycle de développement logiciel.

 

 




