---
description: Msistuff.exe est un utilitaire de ligne de commande qui peut être utilisé pour afficher ou configurer les ressources dans l’exécutable Setup.exe bootstrap.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56d6b183128971501fd3ad8ddb7a88d08cee70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021310"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe est un utilitaire de ligne de commande qui peut être utilisé pour afficher ou configurer les ressources dans l’exécutable Setup.exe bootstrap.

cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Syntaxe

option de **setup.exeMsistuff** *{value}*

Si aucune donnée n’est spécifiée après une option, cette ressource est supprimée.

## <a name="command-line-options"></a>Options de la ligne de commande

Msistuff.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret. Si une option est listée plusieurs fois, seule la dernière occurrence est utilisée.



| Option               | ID de ressource                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| aucune option spécifiée |                              | Affichez les ressources configurables dans Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME, \_ BASEURL      | Définissez BaseURL, l’emplacement de l’URL de base de Setup.exe. Si aucune valeur n’est présente, l’emplacement de Setup.exe est défini par défaut sur support amovible. Seules les installations basées sur une URL sont soumises à un contrôle avec [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust). La barre oblique de fin sur l’URL est facultative. Cette option peut être omise.                                                                                                                                                                                                                     |
| **-d**               | \_base de données ISETUPPROPNAME     | Définissez MSI, le nom du fichier .msi. Il s’agit d’un chemin d’accès relatif au fichier .msi par rapport à l’emplacement du programme Setup.exe. Cette option est requise si l’option-m n’est pas spécifiée. Les options-d et-m s’excluent mutuellement. Elles ne peuvent pas être spécifiées à la fois.                                                                                                                                                                                                                                                    |
| **-m**               | \_correctif ISETUPPROPNAME        | Définissez MSP, le nom du fichier. msp. Il s’agit d’un chemin d’accès relatif au fichier. msp par rapport à l’emplacement du programme Setup.exe. Cette option est requise si l’option-d n’est pas spécifiée. Les options-m et-d s’excluent mutuellement. Elles ne peuvent pas être spécifiées à la fois.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ ProductName  | Définissez le nom du produit, le nom du produit. Cela fournit le nom utilisé dans le texte de la bannière pour l’interface utilisateur téléchargée. Cette option peut être omise. En cas d’omission, la valeur par défaut est « the product ».                                                                                                                                                                                                                                                                                                                            |
| **-o**               | \_opération ISETUPPROPNAME    | Spécifiez le type d’opération à effectuer. Les valeurs valides sont INSTALL, MINPATCH, MAJPATCH et INSTALLUPD. Pour plus d’informations sur ces options, consultez [démarrage du téléchargement Internet](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | \_MSI minimal \_ ISETUPPROPNAME | définir la version Msi minimale, la version minimale de Windows Installer requise sur l’ordinateur. si la version minimale de la Windows Installer n’est pas présente sur l’ordinateur, la [Instmsi.exe](instmsi-exe.md) appropriée est installée pour mettre à niveau le Windows Installer. La valeur de cette propriété a le même format que la \_ valeur PageCount PID. Consultez la propriété [**Résumé du nombre de pages**](page-count-summary.md) . la valeur doit être au moins égale à 200, la valeur de la Windows Installer version 2,0. Cette option est obligatoire. |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | définir l’emplacement de l’url InstMsi, l’emplacement de l’url de base des exécutables de mise à niveau Windows Installer. Si cette valeur est manquante, l’emplacement des fichiers exécutables de mise à niveau est défini par défaut à l’emplacement de Setup.exe. Cette option peut être omise.                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIA     | définissez InstMsiA, le nom de la version ANSI de Windows Installer fichier exécutable de mise à niveau. Il s’agit d’un chemin d’accès relatif à la version ANSI de Instmsi.exe relative à l’emplacement spécifié par ISETUPPROPNAME \_ INSTLOCATION. Cette option est obligatoire.                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | définissez InstMsiW, le nom de la version Unicode de Windows Installer fichier exécutable de mise à niveau. Il s’agit d’un chemin d’accès relatif à la version Unicode de Instmsi.exe relative à l’emplacement spécifié par ISETUPPROPNAME \_ INSTLOCATION. Cette option est obligatoire.                                                                                                                                                                                                                                                                             |
| **-p**               | \_Propriétés ISETUPPROPNAME   | Définissez les chaînes PROPERTY = VALUE. Il s’agit des paires propriété = valeur à inclure sur la ligne de commande. Cette option peut être omise. Cette option ne peut pas être listée plusieurs fois et doit être listée en dernier sur la ligne de commande. L’intégralité de la ligne de commande suivante-p est considérée comme une partie de {value}.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Outils de développement du programme d’installation](windows-installer-development-tools.md)
</dt> <dt>

[Amorçage du téléchargement Internet](internet-download-bootstrapping.md)
</dt> <dt>

[exemple d’Installation Windows Installer basée sur une URL](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
