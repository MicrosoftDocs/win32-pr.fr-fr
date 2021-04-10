---
description: Windows Installer s’exécute en tant que service sur les ordinateurs utilisant Windows 32 bits ou 64 bits.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: À propos des Windows Installer sur les systèmes d’exploitation 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "104211113"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>À propos des Windows Installer sur les systèmes d’exploitation 64 bits

Windows Installer s’exécute en tant que service sur les ordinateurs utilisant Windows 32 bits ou 64 bits. Les versions du programme d’installation antérieures à la version 2,0 peuvent installer et gérer des packages Windows Installer 32 bits uniquement sur les systèmes d’exploitation 32 bits. Notez que vous ne pouvez pas publier ou installer une application 64 bits sur un système d’exploitation 32 bits.

Un package de Windows Installer doit être spécifié en tant que package 32 bits ou 64 bits ; elle ne peut pas être spécifiée comme neutre. Sur un ordinateur qui utilise un système d’exploitation 64 bits, le service Windows Installer est hébergé dans un processus 64 bits qui installe les packages 32 bits et 64 bits. Windows Installer installe trois types de packages Windows Installer sur un ordinateur exécutant un système d’exploitation 64 bits :

-   Packages 32 bits qui contiennent uniquement des composants 32 bits.
-   Packages 64 bits contenant des composants 32 bits.
-   Packages 64 bits contenant uniquement des composants de 64 bits.

Les sections suivantes décrivent les deux types de Windows Installer packages et les nouvelles propriétés de programme d’installation fournies par Windows Installer pour les packages 64 bits.

[Packages de Windows Installer 32 bits](32-bit-windows-installer-packages.md)

[Packages de Windows Installer 64 bits](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de packages Windows Installers 64 bits](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



