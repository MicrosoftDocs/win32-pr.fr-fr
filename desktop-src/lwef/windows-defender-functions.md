---
title: Windows Defender Mission
description: Fonctions appelées par les applications pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ecfa00a38c2263fe1db1b996bb3ec052f8caef1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483125"
---
# <a name="windows-defender-functions"></a>Windows Defender Mission

Fonctions appelées par les applications pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.




| Fonction | Description | 
|----------|-------------|
| <a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a> | Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.<br /> | 
| <a href="mpfreememory.md"><strong>MpFreeMemory</strong></a> | Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.<br /> | 
| <a href="mphandleclose.md"><strong>MpHandleClose</strong></a> | Ferme le handle retourné par <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>ou <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br /> | 
| <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a> | Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.<br /> | 
| <a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a> | <strong>Non pris en charge</strong>. Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.<br /> | 
| <a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a> | Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.<br /> | 
| <a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a> | Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.<br /> | 
| <a href="mpscancontrol.md"><strong>MpScanControl</strong></a> | Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.<br /> | 
| <a href="mpscanstart.md"><strong>MpScanStart</strong></a> | Démarre une opération d’analyse.<br /> | 
| <a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a> | Retourne des informations sur la menace suivante dans la liste d’énumération. Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.<br /> | 
| <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a> | Retourne un handle d’énumération à des fins de récupération des menaces. Cette fonction peut être utilisée pour ouvrir les menaces détectées par une analyse spécifique, toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou toutes les menaces présentes dans la base de données de signature.<br /> | 
| <a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a> | Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.<br /> | 
| <a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a> | Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.<br /> | 
| <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a> | Démarre une opération de mise à jour de signature.<br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> | modifie Windows Defender état sur activé ou désactivé.<br /><blockquote>[!Note]<br />à compter de Windows 10, version 1607 et Windows Server 2016, la fonction <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> retourne toujours <strong>E_NOTIMPL</strong>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a> | Retourne l’état actuel de Windows Defender.<br /> | 




 

 

 





