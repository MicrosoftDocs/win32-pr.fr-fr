---
title: Installation d’applications sur des systèmes 64 bits
description: l’Windows Installer 64 bits peut installer en toute transparence des applications MSI 32 bits sur les Windows 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- installation de l’application 64-bit Windows programmation
- installation 64 bits Windows programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f06eaa527142145791e4ed29e2420d16b1d7a2f4fbe9a77801857a844ed7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643599"
---
# <a name="application-installation-on-64-bit-systems"></a>Installation d’applications sur des systèmes 64 bits

l' [Windows Installer 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) peut installer en toute transparence des applications MSI 32 bits sur les Windows 64 bits. pour les applications plus anciennes qui utilisent un stub 16 bits pour lancer un moteur d’installation 32 bits, le Windows 64 bits reconnaît des programmes d’installation 16 bits spécifiques et remplace une version de 32 bits.

les applications DOS, Windows ou OS/2 16 bits utilisent souvent un stub 16 bits pour vérifier le type de machine, puis lancent un moteur d’installation 32 bits pour effectuer l’installation. pour permettre l’installation d’applications qui utilisent cette technique, 64 bits Windows substitue les versions 32 bits des programmes d’installation 16 bits suivants :

* programme d’installation de Microsoft pour Windows 1,2  
* programme d’installation de Microsoft pour Windows 2,6  
* programme d’installation de Microsoft pour Windows 3,0  
* programme d’installation de Microsoft pour Windows 3,01  
* InstallShield 5. x  

la liste des substitutions est stockée dans le registre sous la clé suivante : **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Ce mécanisme est fourni uniquement pour la compatibilité avec les applications 32 bits qui utilisent les programmes Microsoft installer 16 bits indiqués dans cette rubrique. L’ajout de programmes d’installation tiers n’est pas pris en charge.

 

> [!Note]  
> ce mécanisme n’est pas inclus sur Windows 10 sur ARM.

 

 

 