---
description: Windows Management Instrumentation (WMI) dispose d’une nouvelle clé de Registre pour activer ou désactiver la fonctionnalité de référentiel de restauration.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Clé de Registre pour la configuration du référentiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524132"
---
# <a name="registry-key-for-repository-configuration"></a>Clé de Registre pour la configuration du référentiel

Windows Management Instrumentation (WMI) dispose d’une nouvelle clé de Registre pour activer ou désactiver la fonctionnalité de référentiel de restauration. Pour plus d’informations sur la restauration de l’espace de stockage WMI, consultez [sauvegarder ou restaurer l’espace de stockage WMI](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).

Dans Windows 7, le comportement par défaut consiste à restaurer automatiquement un référentiel à partir d’une version sauvegardée en cas de détection d’un dépôt. WMI fournit la valeur de Registre **AutoRestoreEnabled** pour désactiver cette fonctionnalité.

Les clés de Registre pour WMI se trouvent dans le registre de la clé **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

<dl> <dt>

<span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**
</dt> <dd>

Permet à l’utilisateur de déterminer s’il faut ou non utiliser la fonctionnalité de référentiel autorestauration. Par défaut, cette clé a la valeur 1 et la fonctionnalité de référentiel de la restauration est activée.

Les paramètres suivants sont possibles :

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Désactivé

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

activé

</dd> </dl> </dd> </dl>

La valeur de Registre **AutoRestoreEnabled** peut être modifiée à l’aide de la console de gestion des stratégies de groupe (GPMC). Pour plus d’informations, consultez [console de gestion des stratégies de groupe](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Cette procédure fournit des détails sur l’activation ou la désactivation de la fonctionnalité de référentiel de restauration autorestauration :

**Pour modifier la valeur par défaut de la clé **AutoRestoreEnabled** à l’aide de stratégie de groupe**

1.  Ouvrez la console GPMC.
2.  Créez un objet stratégie de groupe (GPO).
3.  Modifiez l’objet de stratégie de groupe.
4.  Accédez à Préférences/Paramètres Windows/registre.
5.  Cliquez avec le bouton droit et sélectionnez **nouveau... Registre**. Cette action présente une interface utilisateur dans laquelle vous pouvez entrer des informations de registre.
6.  Sélectionnez la commande **mettre à jour** .
7.  Sélectionnez le chemin d’accès de clé de Registre suivant : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM**.
8.  Dans le champ **nom** , entrez **AutoRestoreEnabled**.
9.  Dans le champ **données** , entrez 0 pour désactiver ou 1 pour activer la fonctionnalité de référentiel de restauration.
10. Cliquez sur OK.

 

 
