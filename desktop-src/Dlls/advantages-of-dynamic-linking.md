---
description: La liaison dynamique présente les avantages suivants par rapport à la liaison statique.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Avantages de la liaison dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519942"
---
# <a name="advantages-of-dynamic-linking"></a>Avantages de la liaison dynamique

La liaison dynamique présente les avantages suivants par rapport à la liaison statique :

-   Plusieurs processus qui chargent la même DLL à la même adresse de base partagent une seule copie de la DLL dans la mémoire physique. Cela permet d’économiser la mémoire système et de réduire l’échange.
-   Lorsque les fonctions d’une DLL changent, les applications qui les utilisent n’ont pas besoin d’être recompilées ou reliées tant que les arguments de fonction, les conventions d’appel et les valeurs de retour ne sont pas modifiés. En revanche, le code objet lié statiquement exige que l’application soit reliée lorsque les fonctions changent.
-   Une DLL peut fournir un support après le marché. Par exemple, une DLL de pilote d’affichage peut être modifiée pour prendre en charge un affichage qui n’était pas disponible lors de la livraison initiale de l’application.
-   Les programmes écrits dans différents langages de programmation peuvent appeler la même fonction DLL tant que les programmes suivent la même convention d’appel que celle utilisée par la fonction. La Convention d’appel (par exemple, C, Pascal ou appel standard) contrôle l’ordre dans lequel la fonction appelante doit envoyer les arguments sur la pile, si la fonction ou la fonction appelante est responsable du nettoyage de la pile et si des arguments sont passés dans les registres. Pour plus d’informations, consultez la documentation fournie avec votre compilateur.

Un inconvénient potentiel de l’utilisation des dll est que l’application n’est pas autonome ; Cela dépend de l’existence d’un module DLL distinct. Le système met fin aux processus à l’aide de la liaison dynamique au moment du chargement s’ils requièrent une DLL qui est introuvable lors du démarrage du processus et envoie un message d’erreur à l’utilisateur. Le système ne met pas fin à un processus à l’aide de la liaison dynamique au moment de l’exécution dans ce cas, mais les fonctions exportées par la DLL manquante ne sont pas disponibles pour le programme.

 

 



