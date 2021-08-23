---
description: pour créer des applications Tablet pc en C \# et Visual Basic .net, votre projet dans Microsoft Visual Studio .net doit inclure une référence aux assemblys de la bibliothèque gérée tablet PC. Cela permet d’accéder au modèle d’objet managé et aux contrôles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Bibliothèque et contrôles managés (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d031a97226d200b99a6d36b42e3e4c43862f5b6ac52203ee4ca08d1e5714f2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031727"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Bibliothèque et contrôles managés (Tablet PC)

pour créer des applications Tablet pc en C \# et Visual Basic .net, votre projet dans Microsoft Visual Studio .net doit inclure une référence aux assemblys de la bibliothèque gérée tablet PC. Cela permet d’accéder au modèle d’objet managé et aux contrôles.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# et Visual Basic .net

dans Windows Vista, les assemblys de la bibliothèque gérée Tablet PC sont installés par défaut dans deux répertoires :

-   <systemdrive>: \\ Program Files fichiers \\ communs \\ répertoires Microsoft Shared \\ Ink
-   <systemdrive>: \\ Program Files \\ Microsoft kits \\ Windows \\ v 6.0 \\ Bin

pour ajouter une référence aux bibliothèques gérées de la plateforme Tablet PC dans Microsoft Visual Studio .net :

1.  ouvrez votre projet Visual Studio .net.
2.  Dans le menu **Projet**, cliquez sur **Ajouter une référence**.
3.  Sous l’onglet **.net** de la boîte de dialogue **Ajouter une référence** , dans la liste des composants, sélectionnez **API Microsoft Tablet PC**.
4.  Cliquez sur **Sélectionner**, puis sur **OK**.

pour ajouter une référence aux api d’analyse d’encre dans Visual Studio .net :

1.  ouvrez votre projet Microsoft Visual Studio .net.
2.  Dans le menu **Projet**, cliquez sur **Ajouter une référence**.
3.  Sous l’onglet **.net** de la boîte de dialogue **Ajouter une référence** , dans la liste des composants, sélectionnez **bibliothèque managée d’analyse Microsoft Tablet PC Ink**.
4.  Cliquez sur **Sélectionner**, puis sur **OK**.

> [!Note]  
> lors de la compilation d’applications qui utilisent Microsoft. Ink sur Visual Studio 2005, vous devez sélectionner **Project**, sélectionnez **propriétés**, puis **générer** et définir la plateforme cible = x86. cette option n’est pas disponible dans les produits Microsoft Visual Studio Express.

 

 

 



