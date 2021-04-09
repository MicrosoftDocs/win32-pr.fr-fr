---
description: Windows Installer pouvez utiliser des signatures numériques pour détecter les ressources endommagées.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Signatures numériques et fichiers CAB externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866338"
---
# <a name="digital-signatures-and-external-cabinet-files"></a>Signatures numériques et fichiers CAB externes

Windows Installer pouvez utiliser des signatures numériques pour détecter les ressources endommagées. Lors de l’installation d’une ressource externe, le certificat de signataire appartenant à la ressource peut être vérifié par rapport à un certificat de signataire de référence créé dans le package. Le programme d’installation ne peut pas vérifier les signatures des armoires internes. Il peut uniquement vérifier les signatures numériques à l’aide de la [table MsiDigitalSignature](msidigitalsignature-table.md) et de la [table MsiDigitalCertificate](msidigitalcertificate-table.md).

Windows Installer effectue les opérations suivantes lors de l’installation d’un fichier stocké dans un fichier CAB externe :

-   Le programme d’installation vérifie si l’entrée de support pour ce fichier CAB externe est indiquée dans la [table MsiDigitalSignature](msidigitalsignature-table.md). Un fichier stocké dans un fichier CAB externe est identifié par une entrée dans la colonne Cabinet de la [table multimédia](media-table.md) qui n’est pas préfixée par un \# caractère «».
-   Avant d’ouvrir le fichier CAB externe, le programme d’installation appelle WinVerifyTrust pour extraire le certificat actuel et les informations de hachage. En cas de discordance entre les informations de signature actuelles sur le cabinet et les informations de signature créées dans le package, l’installation échoue. L’installation échoue car le fichier CAB a peut-être été compromis et ne peut pas être approuvé.

Pour plus d’informations sur l’utilisation de signatures numériques, de certificats numériques et de [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), consultez la section [sécurité](https://msdn.microsoft.com/library/cc527452.aspx) du kit de développement logiciel (SDK) Microsoft Windows.

Pour plus d’informations, consultez [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [table MsiDigitalCertificate](msidigitalcertificate-table.md)et [table MsiDigitalSignature](msidigitalsignature-table.md).

 

 
