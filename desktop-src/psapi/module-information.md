---
title: Informations sur le module
description: Un module est un fichier exécutable ou une DLL.
ms.assetid: e15b5e15-ca06-4733-bd0a-705058ba2db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625877832b7e57e68ec6baff79f0c34b4478176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382063"
---
# <a name="module-information"></a>Informations sur le module

Un *module* est un fichier exécutable ou une dll. Chaque processus est constitué d'un ou de plusieurs modules. Vous pouvez récupérer la liste des descripteurs de module pour un processus en appelant la fonction [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) . Cette fonction remplit un tableau de valeurs **HMODULE** avec les handles de module pour le processus spécifié. Le premier module est le fichier exécutable. N’oubliez pas que ces handles de module sont très probablement issus d’autres processus, vous ne pouvez donc pas les utiliser avec des fonctions telles que [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea). Toutefois, vous pouvez utiliser les [fonctions PSAPI](psapi-functions.md) pour obtenir des informations sur un module à partir d’un autre processus.

La procédure suivante décrit comment obtenir des informations de module à partir d’un autre processus.

**Pour obtenir des informations de module à partir d’un autre processus**

1.  Appelez la fonction [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) . Cette fonction prend un handle de processus et un handle de module comme entrée et remplit une mémoire tampon avec le nom de base d’un module (par exemple, Kernel32.dll). Une fonction associée, [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa), accepte les mêmes paramètres que l’entrée, mais retourne le chemin d’accès complet au module (par exemple, C : \\ Windows \\ system32 \\Kernel32.dll).
2.  Appelez la fonction [**GetModuleInformation**](/windows/desktop/api/Psapi/nf-psapi-getmoduleinformation) . Cette fonction accepte un handle de processus et un handle de module et remplit une structure [**MODULEINFO**](/windows/desktop/api/Psapi/ns-psapi-moduleinfo) avec l’adresse de chargement du module, la taille de l’espace d’adressage linéaire qu’elle occupe et un pointeur vers son point d’entrée.

Si une application requiert des informations de module pour le processus en cours, elle doit utiliser la fonction [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) au lieu des fonctions de module PSAPI. Cela permet d’obtenir des performances d’application de deux manières : la fonction **GetModuleFileName** est plus efficace que les fonctions de module psapii, et une application peut éviter de charger psapi.dll si elle n’utilise pas de fonctions PSAPI.

Les fonctions [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) et [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) sont principalement conçues pour être utilisées par les débogueurs et les applications similaires qui doivent extraire les informations de module d’un autre processus. Si la liste de modules dans le processus cible est endommagée ou n’est pas encore initialisée, ou si la liste de modules change pendant l’appel de fonction suite au chargement ou au déchargement de dll, ces fonctions peuvent échouer ou retourner des informations incorrectes.

 

 