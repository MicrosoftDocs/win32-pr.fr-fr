---
title: Fonctions Windows Defender
description: Fonctions appelées par les applications pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381427"
---
# <a name="windows-defender-functions"></a>Fonctions Windows Defender

Fonctions appelées par les applications pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Fonction</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></td>
<td>Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.<br/></td>
</tr>
<tr class="even">
<td><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></td>
<td>Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.<br/></td>
</tr>
<tr class="odd">
<td><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></td>
<td>Ferme le handle retourné par <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>ou <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></td>
<td>Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></td>
<td><strong>Non pris en charge.</strong> Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.<br/></td>
</tr>
<tr class="even">
<td><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></td>
<td>Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></td>
<td>Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.<br/></td>
</tr>
<tr class="even">
<td><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></td>
<td>Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpscanstart.md"><strong>MpScanStart</strong></a></td>
<td>Démarre une opération d’analyse.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></td>
<td>Retourne des informations sur la menace suivante dans la liste d’énumération. Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></td>
<td>Retourne un handle d’énumération à des fins de récupération des menaces. Cette fonction peut être utilisée pour ouvrir les menaces détectées par une analyse spécifique, toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou toutes les menaces présentes dans la base de données de signature.<br/></td>
</tr>
<tr class="even">
<td><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></td>
<td>Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.<br/></td>
</tr>
<tr class="odd">
<td><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></td>
<td>Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></td>
<td>Démarre une opération de mise à jour de signature.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></td>
<td>Modifie l’état de Windows Defender à activé ou désactivé.<br/>
<blockquote>
[!Note]<br />
À compter de Windows 10, version 1607 et Windows Server 2016, la fonction <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> retourne toujours <strong>E_NOTIMPL</strong>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></td>
<td>Retourne l’état actuel de Windows Defender.<br/></td>
</tr>
</tbody>
</table>



 

 

 





