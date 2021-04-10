---
title: Installation d’applications sur des systèmes 64 bits
description: L’Windows Installer 64 bits peut installer en toute transparence des applications MSI 32 bits sur Windows 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- installation d’application 64 bits (programmation Windows)
- installation de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101905"
---
# <a name="application-installation-on-64-bit-systems"></a>Installation d’applications sur des systèmes 64 bits

L' [Windows Installer 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) peut installer en toute transparence des applications MSI 32 bits sur Windows 64 bits. Pour les applications plus anciennes qui utilisent un stub 16 bits pour lancer un moteur d’installation 32 bits, Windows 64 bits reconnaît des programmes d’installation 16 bits spécifiques et remplace une version de 32 bits par un port.

les applications DOS, Windows ou OS/2 16 bits utilisent souvent un stub 16 bits pour vérifier le type de machine, puis lancent un moteur d’installation 32 bits pour effectuer l’installation. Pour permettre l’installation d’applications qui utilisent cette technique, Windows 64 bits remplace les versions 32 bits des programmes d’installation 16 bits suivants :

* Programme d’installation de Microsoft pour Windows 1,2  
* Programme d’installation de Microsoft pour Windows 2,6  
* Programme d’installation de Microsoft pour Windows 3,0  
* Programme d’installation de Microsoft pour Windows 3,01  
* InstallShield 5. x  

La liste des substitutions est stockée dans le Registre sous la clé suivante : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Ce mécanisme est fourni uniquement pour la compatibilité avec les applications 32 bits qui utilisent les programmes Microsoft installer 16 bits indiqués dans cette rubrique. L’ajout de programmes d’installation tiers n’est pas pris en charge.

 

> [!Note]  
> Ce mécanisme n’est pas inclus sur Windows 10 sur ARM.

 

 

 