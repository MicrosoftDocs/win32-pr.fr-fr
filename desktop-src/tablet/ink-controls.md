---
description: Vue d’ensemble des contrôles manuscrits pour Tablet PC.
ms.assetid: 03229b86-f59b-4946-8816-fa153af57630
title: Contrôles Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1206c5e77c12c31a80dcfbca0bebf317a28e0e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525966"
---
# <a name="ink-controls"></a>Contrôles Ink

La plateforme Tablet PC fournit deux contrôles, [InkEdit](inkedit-control.md) et [InkPicture](inkpicture-control.md), qui vous permettent d’ajouter facilement la reconnaissance de l’écriture manuscrite et de l’écriture manuscrite aux applications Tablet PC. Le contrôle InkEdit a des versions [managées](/previous-versions/ms835842(v=msdn.10)), [ActiveX](inkedit-control-reference.md) et Win32, tandis que InkPicture n’a que les versions d' [InkPicture](/previous-versions/ms583740(v=vs.100)) et [ActiveX](inkpicture-control-reference.md) gérées.

La principale différence entre les contrôles réside dans la façon dont les données sont enregistrées. Le contrôle [InkEdit](inkedit-control.md) enregistre l’encre sous forme de texte par défaut, tandis que [InkPicture](inkpicture-control.md) enregistre l’encre sous forme d’encre.

Le contrôle [InkEdit](inkedit-control.md) est destiné à l’entrée de texte via la reconnaissance de l’écriture manuscrite. [InkPicture](inkpicture-control.md) est destiné à l’annotation (par exemple, en marquant une diapositive de présentation ou une autre image).

Dans le code managé, créez des contrôles Ink dans le même thread que le thread principal pour le formulaire. Si un contrôle [InkEdit](inkedit-control.md) ou [InkPicture](inkpicture-control.md) est créé dans un thread différent, il se peut que votre application ne réponde pas correctement.

Vous devez définir explicitement le modèle de thread sur STA (single-thread Apartment) avant de créer un contrôle Ink. Le contrôle est alors créé sur le thread principal. Vous pouvez utiliser le code C++ managé suivant pour définir explicitement le modèle de thread.


```C++
Thread::get_CurrentThread()->set_ApartmentState(ApartmentState::STA);
```



Vous pouvez utiliser le code suivant pour effectuer la même opération en C \# .


```C++
System.Threading.Thread.CurrentThread.ApartmentState = System.Threading.ApartmentState.STA;
```



Dans le code managé, pour éviter une fuite de mémoire, vous devez appeler explicitement la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) sur tout contrôle Tablet PC auquel un gestionnaire d’événements a été attaché avant que le contrôle ne soit hors de portée.

Les sections suivantes décrivent les contrôles Ink et l’utilisation des contrôles Ink dans les applications :

-   [Ajout de contrôles Ink à un projet](adding-ink-controls-to-a-project.md)
-   [InkEdit, contrôle](inkedit-control.md)
-   [Contrôle InkPicture](inkpicture-control.md)

 

 
