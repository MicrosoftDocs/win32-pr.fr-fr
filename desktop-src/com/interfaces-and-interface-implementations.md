---
title: Interfaces et implémentations d’interface
description: COM fait une distinction fondamentale entre les définitions d’interface et leurs implémentations.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee00521b847acbd063f1cd7ad84a0eb231f78d7bd274b7a4658996dbdd61150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992699"
---
# <a name="interfaces-and-interface-implementations"></a>Interfaces et implémentations d’interface

COM fait une distinction fondamentale entre les définitions d’interface et leurs implémentations.

Une *interface* est en fait un contrat qui se compose d’un groupe de prototypes de fonction associés dont l’utilisation est définie mais dont l’implémentation n’est pas. Ces prototypes de fonction sont équivalents à des classes de base virtuelles pures en programmation C++. Une définition d’interface spécifie les fonctions membres de l’interface, appelées *méthodes*, leurs types de retour, le nombre et les types de leurs paramètres, et ce qu’ils doivent faire. Aucune implémentation n’est associée à une interface.

Une *implémentation d’interface* est le code fourni par un programmeur pour effectuer les actions spécifiées dans une définition d’interface. Les implémentations de nombreuses interfaces qu’un programmeur peut utiliser dans une application basée sur un objet sont incluses dans les bibliothèques COM. Toutefois, les programmeurs sont libres d’ignorer ces implémentations et d’écrire leurs propres implémentations. Une implémentation d’interface doit être associée à un objet lorsqu’une instance de cet objet est créée, et l’implémentation fournit les services offerts par l’objet.

Par exemple, une interface hypothétique nommée IStack peut définir deux méthodes, nommées push et pop, en spécifiant que les appels successifs à la méthode pop retournent, dans l’ordre inverse, les valeurs passées précédemment à la méthode push. Cette définition d’interface ne spécifie pas comment les fonctions doivent être implémentées dans le code. Dans l’implémentation de l’interface, un programmeur peut implémenter la pile en tant que tableau et implémenter les méthodes push et pop de manière à accéder à ce tableau, tandis qu’un autre programmeur peut utiliser une liste liée et implémenter les méthodes en conséquence. Quelle que soit l’implémentation particulière des méthodes push et pop, la représentation en mémoire d’un pointeur vers une interface IStack et, par conséquent, son utilisation par un client, est complètement déterminée par la définition de l’interface.

Les objets simples ne prennent en charge qu’une seule interface. Les objets plus compliqués, tels que les objets incorporables, prennent généralement en charge plusieurs interfaces. Les clients ont accès à un objet COM uniquement par le biais d’un pointeur vers l’une de ses interfaces, qui, à son tour, permet au client d’appeler l’une des méthodes qui composent cette interface. Ces méthodes déterminent la façon dont un client peut utiliser les données de l’objet.

Les interfaces définissent un contrat entre un objet et ses clients. Le contrat spécifie les méthodes qui doivent être associées à chaque interface et le comportement de chacune des méthodes en termes d’entrée et de sortie. Le contrat ne définit généralement pas comment implémenter les méthodes dans une interface. Un autre aspect important du contrat est que si un objet prend en charge une interface, il doit prendre en charge toutes les méthodes de cette interface de quelque façon que ce soit. Toutes les méthodes d’une implémentation n’ont pas besoin de faire quoi que ce soit. Si un objet ne prend pas en charge la fonction impliquée par une méthode, son implémentation peut être un retour simple ou éventuellement le retour d’un message d’erreur explicite, mais les méthodes doivent exister.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets et interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




