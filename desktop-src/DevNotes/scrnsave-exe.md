---
description: '\\Bureau du panneau de configuration HKCU \\ .'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393159"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**\\Bureau du panneau de configuration HKCU \\**



| Type de données | Plage       | Valeur par défaut |
|-----------|-------------|---------------|
| SZ de REG \_   | *Nom de fichier* | (aucune)        |



 

## <a name="description"></a>Description

Spécifie le nom du fichier exécutable de l’écran de veille.

## <a name="change-method"></a>Modifier la méthode

Pour modifier la valeur de cette entrée, dans Panneau de configuration, double-cliquez sur **affichage**, cliquez sur l’onglet **écran de veille** , puis sélectionnez un écran de veille dans la liste **écran de veille** .

Vous pouvez également modifier cette entrée à l’aide de la fonction d’interface de programmation d’applications (API) **InstallScreenSaver**, qui est exportée par Desk.cpl. Vous pouvez accéder à cette fonction à l’aide de la ligne de commande **rundll32.exe desk.cpl,** *fichier* InstallScreenSaver, où *fichier* est le nom d’un fichier exécutable de l’écran de veille.

## <a name="activation-method"></a>Méthode d’activation

Les modifications apportées à cette entrée deviennent effectives lors du prochain démarrage de l’économiseur d’écran par le système. Les modifications apportées à cette entrée pendant l’exécution d’un économiseur d’écran n’ont aucun effet sur l’écran de veille.

## <a name="notes"></a>Notes

-   Les systèmes d’exploitation Windows ajoutent cette entrée au registre lorsque vous utilisez l’option **Afficher** du panneau de configuration pour sélectionner un économiseur d’écran. Si vous désactivez tous les économiseurs d’écran en choisissant **(aucun)** dans la liste écran de veille, le système d’exploitation supprime cette entrée du Registre et appelle la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec *uiaction* égal à SPI \_ SETSCREENSAVEACTIVE et *uiParam* égal à **false**.
-   Cette entrée peut être remplacée par un paramètre de stratégie de groupe sur les systèmes qui prennent en charge stratégie de groupe. Lorsque le paramètre stratégie de groupe du nom de l’exécutable de l' **économiseur d’écran** est activé, le système ignore cette entrée. La configuration de ce paramètre de stratégie est stockée dans l’entrée **SCRNSAVE.EXE** , qui se trouve dans la sous-clé **stratégies** .

 

 
