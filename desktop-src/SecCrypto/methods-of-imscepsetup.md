---
description: Méthodes définies par l’interface IMSCEPSetup.
ms.assetid: 0d41243f-cff1-4608-bbe6-f99dc548b0e2
title: Méthodes de IMSCEPSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f543bb4525a3335128846ec5724e1a9a09a35f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526733"
---
# <a name="methods-of-imscepsetup"></a>Méthodes de IMSCEPSetup

Les méthodes suivantes sont définies par l’interface [**IMSCEPSetup**](/windows/desktop/api/Casetup/nn-casetup-imscepsetup) . Les méthodes d’accès à la propriété ne sont pas indiquées ici. Pour afficher les propriétés de **IMSCEPSetup**, consultez [Propriétés de IMSCEPSetup](properties-of-imscepsetup.md).



| Méthode                                                             | Description                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getkeylengthlist)           | Obtient la liste des [*longueurs de clé*](../secgloss/k-gly.md) prises en charge par le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) spécifié. |
| [**GetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getmscepsetupproperty) | Obtient une valeur de propriété pour une configuration du service d’inscription d’appareils réseau (NDES).                                                                                                                                                                                               |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-getprovidernamelist)     | Obtient la liste des fournisseurs de services de chiffrement qui fournissent des algorithmes de signature et d’échange de clé asymétrique sur l’ordinateur.                                                                                                                                                                              |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-initializedefaults)       | Initialise un objet **CMSCEPSetup** avec des valeurs par défaut pour permettre l’installation d’un rôle ndes.                                                                                                                                                                                  |
| [**Installer**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-install)                             | Installe un rôle tel que configuré dans l’objet **CMSCEPSetup** .                                                                                                                                                                                                                      |
| [**IsMSCEPStoreEmpty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-ismscepstoreempty)         | Retourne toujours **la \_ valeur variant true** et ne doit pas être utilisée.                                                                                                                                                                                                                          |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-postuninstall)                 | Cette méthode n’est pas implémentée. Elle est réservée pour un usage futur.                                                                                                                                                                                                                    |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-preuninstall)                   | Supprime le registre et les paramètres IIS pour le rôle NDES.                                                                                                                                                                                                                              |
| [**SetAccountInformation**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setaccountinformation) | Définit les informations de compte d’utilisateur utilisées par l’extension NDES IIS pour effectuer une inscription pour le compte de périphériques réseau.                                                                                                                                                              |
| [**SetMSCEPSetupProperty**](/windows/desktop/api/Casetup/nf-casetup-imscepsetup-setmscepsetupproperty) | Définit une valeur de propriété pour une configuration NDES.                                                                                                                                                                                                                                  |



 

 

 
