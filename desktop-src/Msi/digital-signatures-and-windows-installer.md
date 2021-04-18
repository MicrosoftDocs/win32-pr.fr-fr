---
description: La Windows Installer peut utiliser des signatures numériques pour détecter les ressources endommagées.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Signatures numériques et Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d41dee15da938c586bf061d216d9003586a799c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519451"
---
# <a name="digital-signatures-and-windows-installer"></a>Signatures numériques et Windows Installer

La Windows Installer peut utiliser des signatures numériques pour détecter les ressources endommagées. Un certificat de signataire peut être comparé au certificat de signataire d’une ressource externe qui doit être installée par le package. Pour plus d’informations sur l’utilisation de signatures numériques, de certificats numériques et de [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consultez la section [sécurité](https://msdn.microsoft.com/library/cc527452.aspx) du kit de développement logiciel (SDK) Microsoft Windows.

Avec Windows Installer, les signatures numériques peuvent être utilisées avec des packages Windows Installer, des transformations, des correctifs, des modules de fusion et des fichiers CAB externes. Windows Installer est intégré à la stratégie de restriction logicielle sur Microsoft Windows XP. Des stratégies peuvent être créées pour autoriser ou empêcher les installations basées sur des critères différents, y compris un certificat ou un éditeur de signataire particulier. La Windows Installer peut effectuer la validation de signature des fichiers CAB externes sur toutes les plateformes où CryptoAPI version 2,0 est installé.

Notez que l’exemple Setup.exe bootstrap fourni avec le kit de développement logiciel (SDK) Windows Installer effectue une vérification de signature sur un package de Windows Installer avant de lancer l’installation.

L’exécution d’une [installation d’administration](administrative-installation.md) supprime la signature numérique du package. Une installation administrative modifie le package d’installation afin d’ajouter le flux AdminProperties, ce qui invaliderait la signature numérique d’origine. Un administrateur peut abandonner le package.

L’application d’un correctif à une installation d’administration supprime également la signature numérique du package. La raison est que les modifications sont conservées dans le package d’installation corrigé de l’installation d’administration. Un administrateur peut abandonner le package.

À partir de Windows Installer version 3,0, la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md) permet aux utilisateurs non-administrateurs d’appliquer des correctifs aux applications installées dans le contexte par ordinateur. La mise à jour corrective du contrôle de compte d’utilisateur est activée en fournissant un certificat de signataire dans la table [MsiPatchCertificate](msipatchcertificate-table.md) et en signant les correctifs avec le même certificat.

Pour plus d’informations, consultez [signatures numériques et fichiers CAB externes](digital-signatures-and-external-cabinet-files.md), [Windows Installer et stratégie de restriction logicielle](windows-installer-and-software-restriction-policy.md), [création d’une installation signée entièrement vérifiée](authoring-a-fully-verified-signed-installation.md)et [URL basée sur un exemple d’installation Windows Installer](a-url-based-windows-installer-installation-example.md).

 

 
