---
description: Pour créer des applications Tablet PC en C \# et Visual Basic .net, votre projet dans Microsoft Visual Studio .net doit inclure une référence aux assemblys de la bibliothèque gérée Tablet PC. Cela permet d’accéder au modèle d’objet managé et aux contrôles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Bibliothèque et contrôles managés (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536585"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Bibliothèque et contrôles managés (Tablet PC)

Pour créer des applications Tablet PC en C \# et Visual Basic .net, votre projet dans Microsoft Visual Studio .net doit inclure une référence aux assemblys de la bibliothèque gérée Tablet PC. Cela permet d’accéder au modèle d’objet managé et aux contrôles.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# et visual Basic.net

Dans Windows Vista, les assemblys de la bibliothèque gérée Tablet PC sont installés par défaut dans deux répertoires :

-   <systemdrive>: \\ Program Files fichiers \\ communs \\ répertoires Microsoft Shared \\ Ink
-   <systemdrive>: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin

Pour ajouter une référence aux bibliothèques gérées de la plateforme Tablet PC dans Microsoft Visual Studio .NET :

1.  Ouvrez votre projet Visual Studio .NET.
2.  Dans le menu **Projet**, cliquez sur **Ajouter une référence**.
3.  Sous l’onglet **.net** de la boîte de dialogue **Ajouter une référence** , dans la liste des composants, sélectionnez **API Microsoft Tablet PC**.
4.  Cliquez sur **Sélectionner**, puis sur **OK**.

Pour ajouter une référence aux API d’analyse d’encre dans Visual Studio .NET :

1.  Ouvrez votre projet Microsoft Visual Studio .NET.
2.  Dans le menu **Projet**, cliquez sur **Ajouter une référence**.
3.  Sous l’onglet **.net** de la boîte de dialogue **Ajouter une référence** , dans la liste des composants, sélectionnez **bibliothèque managée d’analyse Microsoft Tablet PC Ink**.
4.  Cliquez sur **Sélectionner**, puis sur **OK**.

> [!Note]  
> Lors de la compilation d’applications qui utilisent Microsoft. Ink sur Visual Studio 2005, vous devez sélectionner **projet**, sélectionner **Propriétés**, puis **générer** et définir la plateforme cible = x86. Cette option n’est pas disponible dans les produits Microsoft Visual Studio Express.

 

 

 



