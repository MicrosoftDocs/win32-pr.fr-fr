---
description: Le contrôle WMI est un composant logiciel enfichable MMC situé dans le panneau de configuration et utilisé pour définir manuellement la sécurité de l’espace de noms WMI sur un ordinateur local. Vous pouvez également définir l’espace de noms par défaut pour les scripts.
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: Définition de la sécurité de l’espace de noms avec le contrôle WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524693"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a>Définition de la sécurité de l’espace de noms avec le contrôle WMI

Le contrôle WMI est un composant logiciel enfichable MMC situé dans le **panneau** de configuration et utilisé pour définir manuellement la sécurité de l’espace de noms WMI sur un ordinateur local. Vous pouvez également définir l’espace de noms par défaut pour les scripts.


La procédure suivante décrit comment localiser le contrôle WMI.

**Pour localiser le contrôle WMI**

1.  Dans le **panneau de configuration**, double-cliquez sur **Outils d’administration**.
2.  Dans la fenêtre **Outils d’administration**, double-cliquez sur **Gestion de l’ordinateur**.
3.  Dans la fenêtre Gestion de l' **ordinateur** , développez l’arborescence **services et applications** , puis double-cliquez sur le **contrôle WMI**.
4.  Cliquez avec le bouton droit sur l’icône de **contrôle WMI** et sélectionnez **Propriétés**.

La procédure suivante décrit comment utiliser le contrôle WMI pour configurer la sécurité d’un espace de noms en tant que modèle, puis obtenir par programmation les paramètres de sécurité pour définir la sécurité pour d’autres espaces de noms.

**Pour définir la sécurité de l’espace de noms avec le contrôle WMI**

1.  Créez un espace de noms à l’aide du code format MOF (MOF).
2.  Exécutez le contrôle WMI pour définir la sécurité sur le nouvel espace de noms. Dans le menu **Démarrer** , cliquez sur **exécuter** , tapez **wmimgmt. msc** ou recherchez [le contrôle WMI](#).
3.  Dans le volet de **contrôle WMI** , cliquez avec le bouton droit sur **contrôle WMI**, choisissez **Propriétés**, puis sélectionnez l’onglet **sécurité** .
4.  Accédez au nouvel espace de noms, cliquez sur **sécurité**, puis configurez les groupes et les autorisations pour l’espace de noms.

Vous pouvez également utiliser Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) pour définir la sécurité de l’espace de noms. Pour plus d’informations, consultez [**WMIC**](wmic.md).

## <a name="setting-the-default-namespace-for-scripts"></a>Définition de l’espace de noms par défaut pour les scripts

Si un script ne se connecte pas explicitement à un espace de noms lors de la connexion à WMI, WMI utilise l’espace de noms par défaut spécifié dans ce contrôle. La valeur par défaut se trouve également dans l’entrée du Registre comme suit :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

Étant donné que l’espace de noms par défaut est facile à modifier, soit avec ce contrôle, soit par programmation en appelant des méthodes de [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), spécifiez l’espace de noms lors de la connexion à WMI par le biais du [moniker](constructing-a-moniker-string.md) ou des appels à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md) .

**Pour définir l’espace de noms par défaut pour les scripts**

1.  Dans la fenêtre **Propriétés du contrôle WMI** , choisissez l’onglet **avancé** .
2.  Cliquez sur le bouton **modifier** et sélectionnez l’espace de noms à utiliser comme valeur par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des descripteurs de sécurité des espaces de noms](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
