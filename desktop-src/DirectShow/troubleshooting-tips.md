---
description: Conseils de dépannage
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Conseils de dépannage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531994"
---
# <a name="troubleshooting-tips"></a>Conseils de dépannage

Les conseils suivants vous aideront à éviter les blocages ou les blocages dans votre application DirectShow.

**Objets globaux**

Un objet C++ global ne doit pas créer d’objets DirectShow dans sa méthode de constructeur, ni les libérer dans sa méthode de destructeur. Cela peut entraîner le blocage indéfini de l’application, pour la raison suivante :

Les threads ne peuvent pas se fermer lorsqu’ils se trouvent dans la fonction de point d’entrée d’une DLL. Le noyau 32 contient un verrou de processus global pendant la fonction de point d’entrée, et le verrou empêche le thread de se fermer. Comme certains objets DirectShow possèdent des threads, ils peuvent bloquer s’ils sont libérés dans une fonction de point d’entrée de DLL. Si une application a un objet C++ global, la DLL runtime C appelle le destructeur de l’objet lorsque la DLL est déchargée. Si le destructeur libère des objets DirectShow, il peut en résulter un blocage.

Pour des raisons similaires, une DLL ne doit pas créer ou libérer des objets DirectShow dans sa routine de point d’entrée.

**Libérer des interfaces**

Vous devez libérer tous les pointeurs d’interface DirectShow pendant que votre application traite encore des messages avant de quitter la boucle de message. Dans le cas contraire, vous pouvez voir plusieurs assertions, car certains objets DirectShow envoient des messages pendant leurs routines de nettoyage.

(En tant que corollic, si vous utilisez la classe ATL **CWindowImpl** , n’attendez pas que **OnFinalMessage** libère les interfaces. Au lieu de cela, libérez-les lorsque vous gérez le \_ message WM Close.)

**Nombres de références**

Lorsque la version de débogage de Quartz.dll est déchargée, elle vérifie si des objets DirectShow ont des décomptes de références qui n’ont pas été libérés. Si c’est le cas, elle lève une assertion :


```C++
g_cFGObjects == 0 
```



Lorsque cette assertion échoue, cela signifie que votre application a divulgué un nombre de références. Examinez votre code et assurez-vous de libérer tous les pointeurs d’interface.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage dans DirectShow](debugging-in-directshow.md)
</dt> </dl>

 

 



