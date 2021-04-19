---
description: Bien que les fournisseurs soient encouragés à utiliser des noms d’instance uniques, ce n’est pas le cas de tous les fournisseurs.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Gestion des noms d’instance en double
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 220e5d7d0181a79c1d1415486cc946d484e11952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518477"
---
# <a name="handling-duplicate-instance-names"></a>Gestion des noms d’instance en double

Bien que les fournisseurs soient fortement encouragés à utiliser des noms d’instance uniques, tous les fournisseurs ne le font pas. La Convention d’affichage des noms d’instance en double consiste à ajouter un `#` caractère et un numéro de série au nom de l’instance, à l’exception de la première occurrence du nom. Par exemple, s’il existe trois instances de `svchost` dans un exemple, les trois noms s’affichent sous la forme `svchost` , `svchost#1` et `svchost#2` .

Malheureusement, cette Convention ne résout pas complètement le problème. Les numéros de série sont attribués en fonction de l’ordre dans lequel un nom d’instance particulier apparaît dans un exemple, et cet ordre peut être incohérent de l’exemple à l’exemple. Par exemple, l’exemple A peut voir `svchost` (pid 100), `svchost#1` (PID 200) et `svchost#2` (PID 300). Ensuite, si le svchost avec PID 100 s’arrête, l’exemple suivant peut voir `svchost` (pid 200) et `svchost#1` (PID 300). La logique de correspondance de base tenterait de faire correspondre les statistiques de l’exemple A `svchost#1` (du pid 200) aux statistiques de l’exemple b `svchost#1` (du PID 300), ce qui entraînera des résultats non valides pour l’exemple b. des erreurs se produisent quand une nouvelle instance non unique s’affiche dans un exemple ou lorsqu’une instance non unique s’arrête dans un échantillon (sauf si l’instance ajoutée

## <a name="process-counterset"></a>Process CounterSet

Ce problème est particulièrement problématique pour le `Process` CounterSet, car il utilise uniquement le nom de l’exe du processus comme nom d’instance, même si le nom de l’exe n’est pas unique. Impossible de modifier le comportement par défaut du `Process` CounterSet sur Windows en raison de problèmes de compatibilité.

Vous pouvez modifier le comportement des `Process` countersets et `Thread` pour utiliser des noms d’instance uniques en définissant les `ProcessNameFormat` valeurs de `ThreadNameFormat` Registre ou sous la `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` clé de registre.

> [!CAUTION]
> L’activation de noms d’instance uniques pour le `Process` CounterSet peut entraîner un comportement incorrect de certains programmes, car de nombreux programmes attendent un modèle d’attribution de noms non unique. Par exemple, un programme qui recherche une instance avec un nom d’EXE connu spécifique ne pourra plus trouver cette instance après avoir activé des noms d’instance uniques.

Le type de Registre pour ces valeurs est `REG_DWORD` . La définition de la valeur sur `2` ajoute l’identificateur de processus (PID) au nom d’instance de processus et l’identificateur de thread (TID) au nom d’instance de thread. Pour désactiver cette fonctionnalité, définissez la valeur sur 1 ou supprimez la valeur.
