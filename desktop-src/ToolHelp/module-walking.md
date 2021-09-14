---
title: Parcours du module
description: Un instantané qui inclut la liste des modules pour un processus spécifié contient des informations sur chaque module, fichier exécutable ou bibliothèque de liens dynamiques (DLL), utilisé par le processus spécifié.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- bibliothèques de liens dynamiques
- bibliothèques de liens dynamiques, énumération de dll
- énumérer
- énumération, dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856593"
---
# <a name="module-walking"></a>Parcours du module

Un instantané qui inclut la liste des modules pour un processus spécifié contient des informations sur chaque module, fichier exécutable ou bibliothèque de liens dynamiques (DLL), utilisé par le processus spécifié. Vous pouvez récupérer des informations pour le premier module de la liste à l’aide de la fonction [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) . Après avoir récupéré le premier module de la liste, vous pouvez récupérer des informations pour les modules suivants dans la liste à l’aide de la fonction [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) . **Module32First** et **Module32Next** remplissent une structure [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) avec des informations sur le module.

Vous pouvez récupérer un code d’état d’erreur étendu pour [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) et [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> L’identificateur de module, qui est spécifié dans le membre **th32ModuleID** de [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32), a uniquement une signification en Windows 16 bits.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Parcours de la liste des modules](traversing-the-module-list.md)
</dt> </dl>

 

 