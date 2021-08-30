---
description: Les fonctions de cette section installent et configurent des pilotes d’imprimante sur un ordinateur.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Référence d’installation du pilote d’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627785e4b6b01302358aedb2dc3527949cb688f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470735"
---
# <a name="printer-driver-installation-reference"></a>Référence d’installation du pilote d’imprimante

Les fonctions de cette section installent et configurent des pilotes d’imprimante sur un ordinateur.

## <a name="in-this-section"></a>Dans cette section




| Fonction | Description | 
|----------|-------------|
| <a href="addmonitor.md"><strong>AddMonitor</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> installe un moniteur de port local et lie les fichiers de configuration, de données et de surveillance.<br /> | 
| <a href="addport.md"><strong>AddPort</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/addport"><strong>addport</strong></a> ajoute le nom d’un port à la liste des ports pris en charge. La fonction <strong>addport</strong> est exportée par le moniteur de port.<br /> | 
| <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> installe un pilote d’imprimante local ou distant et associe les fichiers de configuration, de données et de pilote.<br /> Pour une plus grande flexibilité lors de l’installation ou de la mise à niveau des pilotes d’imprimante, utilisez la fonction <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> car elle permet une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers plus récents uniquement et la copie de tous les fichiers (quels que soient les horodatages de fichier).<br /><blockquote>[!Note]<br />L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée. Utilisez <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> à la place.</blockquote><br /> | 
| <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> installe un pilote d’imprimante local ou distant et lie les fichiers de configuration, de données et de pilote. Outre les fonctionnalités de <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, il offre également des options qui permettent une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers récents uniquement et la copie de tous les fichiers (quels que soient les horodatages des fichiers).<br /><blockquote>[!Note]<br />L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée. Utilisez <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> à la place.</blockquote><br /> | 
| <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> installe un processeur d’impression sur le serveur spécifié et ajoute le nom du processeur d’impression à la liste des processeurs d’impression pris en charge.<br /> | 
| <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> installe un fournisseur d’impression local et lie les fichiers de configuration, de données et de fournisseur.<br /> | 
| <a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.<br /> | 
| <a href="deletemonitor.md"><strong>DeleteMonitor</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> supprime un moniteur de port ajouté par la fonction <a href="addmonitor.md"><strong>AddMonitor</strong></a> .<br /> | 
| <a href="deleteport.md"><strong>DeletePort</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> affiche une boîte de dialogue qui permet à l’utilisateur de supprimer un nom de port.<br /> | 
| <a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur.<br /> Pour supprimer les fichiers associés au pilote en plus de supprimer le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge pour un serveur, utilisez la fonction <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .<br /><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> supprime un pilote uniquement si aucune version du pilote n’est utilisée pour l’environnement spécifié. <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> peut supprimer des versions spécifiques du pilote.<br /> | 
| <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur et supprime les fichiers associés au pilote. Cette fonction peut également supprimer des versions spécifiques du pilote.<br /> | 
| <a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a><br /> | Supprime un package de pilotes d’imprimante du magasin de pilotes.<br /> | 
| <a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> supprime un processeur d’impression ajouté par la fonction <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .<br /> | 
| <a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> supprime un fournisseur d’impression ajouté par la fonction <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .<br /> | 
| <a href="enummonitors.md"><strong>EnumMonitors</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> récupère des informations sur les moniteurs de port installés sur le serveur spécifié.<br /> | 
| <a href="enumports.md"><strong>EnumPorts</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> énumère les ports qui sont disponibles pour l’impression sur un serveur spécifié.<br /> | 
| <a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> énumère les pilotes d’imprimante installés sur un serveur d’impression spécifié.<br /> | 
| <a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> énumère les types de données pris en charge par un processeur d’impression spécifié.<br /> | 
| <a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> énumère les processeurs d’impression installés sur le serveur spécifié.<br /> | 
| <a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a><br /> | Récupère le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.<br /> | 
| <a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> récupère les données du pilote pour l’imprimante spécifiée. Si le pilote n’est pas installé sur l’ordinateur local, <strong>GetPrinterDriver</strong> l’installe.<br /> | 
| <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a><br /> | La fonction <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> récupère les données du pilote pour l’imprimante spécifiée. Si le pilote n’est pas installé sur l’ordinateur local, <strong>GetPrinterDriver2</strong> l’installe et affiche l’interface utilisateur dans la fenêtre spécifiée.<br /> | 
| <a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> récupère le chemin d’accès du répertoire du pilote d’imprimante.<br /> | 
| <a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a><br /> | Récupère le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.<br /> | 
| <a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a><br /> | La fonction <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> récupère le chemin d’accès au répertoire du processeur d’impression sur le serveur spécifié.<br /> | 
| <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a><br /> | Installe un pilote d’imprimante à partir d’un package de pilotes qui se trouve dans le magasin de pilotes du serveur d’impression.<br /> | 
| <a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a><br /> | Charge un pilote d’imprimante sur le magasin de pilotes du serveur d’impression afin qu’il puisse être installé en appelant <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.<br /> | 




 

 

