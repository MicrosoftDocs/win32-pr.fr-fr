---
description: 'Chaque processus a un bloc d’environnement qui contient un ensemble de variables d’environnement et leurs valeurs. Il existe deux types de variables d’environnement : les variables d’environnement utilisateur (définies pour chaque utilisateur) et les variables d’environnement système (définies pour tout le monde).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Variables d'environnement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647c685aac8ed6df36c0312d7eef49793fd4b2bbfca5576e0377e59da31dd777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910319"
---
# <a name="environment-variables"></a>Variables d'environnement

Chaque processus a un bloc d’environnement qui contient un ensemble de variables d’environnement et leurs valeurs. Il existe deux types de variables d’environnement : les variables d’environnement utilisateur (définies pour chaque utilisateur) et les variables d’environnement système (définies pour tout le monde).

Par défaut, un processus enfant hérite des variables d’environnement de son processus parent. Les programmes démarrés par le processeur de commande héritent des variables d’environnement du processeur de commandes. Pour spécifier un environnement différent pour un processus enfant, créez un bloc d’environnement et transmettez un pointeur vers celui-ci en tant que paramètre de la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Le processeur de commande fournit la commande **Set** pour afficher son bloc d’environnement ou pour créer de nouvelles variables d’environnement. Vous pouvez également afficher ou modifier les variables d’environnement en sélectionnant **système** dans le **panneau** de configuration, en sélectionnant **paramètres système avancés** et en cliquant sur **variables d’environnement**.

Chaque bloc d’environnement contient les variables d’environnement au format suivant :<dl> *Var1* = *Valeur1* \\ entre  
*Var2* = *Valeur2* \\ entre  
*Var3* = *Valeur3* \\ entre  
...  
*VarN* = *ValeurN* \\ 0 \\ 0  
</dl>

Le nom d’une variable d’environnement ne peut pas inclure un signe égal (=).

La fonction [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) retourne un pointeur vers le bloc d’environnement du processus appelant. Ce doit être traité comme un bloc en lecture seule ; ne le modifiez pas directement. Utilisez plutôt la fonction [**SetEnvironmentVariable ne contient**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) pour modifier une variable d’environnement. Lorsque vous avez terminé avec le bloc d’environnement obtenu à partir de **GetEnvironmentStrings**, appelez la fonction [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) pour libérer le bloc.

L’appel de [**SetEnvironmentVariable ne contient**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) n’a aucun effet sur les variables d’environnement système. Pour ajouter ou modifier des variables d’environnement système par programmation, ajoutez-les à la clé de Registre **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ Environment** , puis diffusez un message [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) avec *lParam* défini sur la chaîne « Environment ». Cela permet aux applications, telles que l’interpréteur de commandes, de récupérer vos mises à jour.

La taille maximale d’une variable d’environnement définie par l’utilisateur est de 32 767 caractères. Il n’existe aucune limitation technique quant à la taille du bloc d’environnement. Toutefois, il existe des limites pratiques en fonction du mécanisme utilisé pour accéder au bloc. Par exemple, un fichier de commandes ne peut pas définir une variable dont la longueur est supérieure à la longueur maximale de la ligne de commande.

**Windows Server 2003 et Windows XP :** La taille maximale du bloc d’environnement pour le processus est de 32 767 caractères. à partir de Windows Vista et Windows Server 2008, il n’existe aucune limitation technique quant à la taille du bloc d’environnement.

La fonction [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) détermine si une variable spécifiée est définie dans l’environnement du processus appelant et, le cas échéant, quelle est sa valeur.

Pour récupérer une copie du bloc d’environnement pour un utilisateur donné, utilisez la fonction [**CreateEnvironmentBlock**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) .

Pour développer des chaînes de variable d’environnement, utilisez la fonction [**ExpandEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modification des variables d’environnement](changing-environment-variables.md)
</dt> <dt>

[Variables d’environnement utilisateur](../shell/user-environment-variables.md)
</dt> </dl>

 

 
