---
description: la Windows Installer peut utiliser des signatures numériques pour détecter les ressources endommagées.
ms.assetid: 68f2c686-cbe0-495d-a448-a7d2ca1df47b
title: Signatures numériques et Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 334cf226d683c9b9a658ce72e25bf7bf90145369c315da372bd6c4e9368b796a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692809"
---
# <a name="digital-signatures-and-windows-installer"></a>Signatures numériques et Windows Installer

la Windows Installer peut utiliser des signatures numériques pour détecter les ressources endommagées. Un certificat de signataire peut être comparé au certificat de signataire d’une ressource externe qui doit être installée par le package. pour plus d’informations sur l’utilisation de signatures numériques, de certificats numériques et de [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consultez la section [sécurité](https://msdn.microsoft.com/library/cc527452.aspx) du kit de développement logiciel (SDK) de Microsoft Windows.

avec Windows Installer, les signatures numériques peuvent être utilisées avec des packages Windows Installer, des transformations, des correctifs, des modules de fusion et des fichiers cab externes. Windows le programme d’installation est intégré à la stratégie de Restriction logicielle sur Microsoft Windows XP. Des stratégies peuvent être créées pour autoriser ou empêcher les installations basées sur des critères différents, y compris un certificat ou un éditeur de signataire particulier. la Windows Installer peut effectuer la validation de signature des fichiers cab externes sur toutes les plateformes où CryptoAPI version 2,0 est installé.

notez que l’exemple Setup.exe bootstrap fourni avec le kit de développement logiciel (SDK) Windows Installer effectue une vérification de signature sur un package de Windows Installer avant de lancer l’installation.

L’exécution d’une [installation d’administration](administrative-installation.md) supprime la signature numérique du package. Une installation administrative modifie le package d’installation afin d’ajouter le flux AdminProperties, ce qui invaliderait la signature numérique d’origine. Un administrateur peut abandonner le package.

L’application d’un correctif à une installation d’administration supprime également la signature numérique du package. La raison est que les modifications sont conservées dans le package d’installation corrigé de l’installation d’administration. Un administrateur peut abandonner le package.

à partir de Windows Installer version 3,0, la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md) permet aux utilisateurs non-administrateurs d’appliquer des correctifs aux applications installées dans le contexte par ordinateur. La mise à jour corrective du contrôle de compte d’utilisateur est activée en fournissant un certificat de signataire dans la table [MsiPatchCertificate](msipatchcertificate-table.md) et en signant les correctifs avec le même certificat.

pour plus d’informations, consultez [Signatures numériques et fichiers cab externes](digital-signatures-and-external-cabinet-files.md), [Windows Installer et stratégie de Restriction logicielle](windows-installer-and-software-restriction-policy.md), [création d’une installation signée entièrement vérifiée](authoring-a-fully-verified-signed-installation.md)et [URL basée sur un exemple d’installation Windows Installer](a-url-based-windows-installer-installation-example.md).

 

 
