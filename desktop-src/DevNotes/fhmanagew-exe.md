---
description: Le programme FhManagew.exe supprime les versions de fichiers qui dépassent un âge spécifié de l’appareil cible de l’historique des fichiers actuellement attribué.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483241"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

Le programme FhManagew.exe supprime les versions de fichiers qui dépassent un âge spécifié de l’appareil cible de l’historique des fichiers actuellement attribué.

Ce programme est disponible dans Windows 8 et Windows Server 2012 et versions ultérieures.

Pour exécuter ce programme, accédez au menu **Démarrer** , cliquez sur **exécuter**, puis tapez la commande suivante.

**FhManagew.exe-âge de nettoyage** 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Paramètre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="age"></span><span id="AGE"></span><em>vieillissement</em><br/></td>
<td>Ce paramètre spécifie l’âge minimal, en jours, des versions de fichiers qui peuvent être supprimées. Une version de fichier est supprimée si les deux conditions suivantes sont remplies :<br/>
<ul>
<li>La version du fichier est antérieure à l’ancienneté spécifiée.</li>
<li>Le fichier n’est plus inclus dans l’étendue de protection ou il existe une version plus récente du même fichier sur l’appareil cible.</li>
</ul>
Si le paramètre <em>Age</em> a la valeur zéro, toutes les versions de fichier sont supprimées, à l’exception de la version la plus récente de chaque fichier actuellement présent dans l’étendue de protection.<br/></td>
</tr>
</tbody>
</table>



 

Pour supprimer toutes les sorties de ce programme, utilisez l’option de ligne de commande **Quiet** comme suit.

**FhManagew.exe-nettoyer** *Age* **-Quiet**

## <a name="examples"></a>Exemples



| Exemple                                                                                                                                                                                                      | Description                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-nettoyage 30**<br/>                                 | Supprimer toutes les versions de fichiers datant de plus d’un mois.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Cleanup 365-quiet**<br/> | Supprimer toutes les versions de fichiers datant de plus d’un an et supprimer toutes les sorties.<br/> |



 

 

 




