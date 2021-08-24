---
description: Les méthodes suivantes sont définies par l’interface ICertSrvSetup. Les méthodes d’accès à la propriété ne sont pas indiquées ici. Pour afficher les propriétés de ICertSrvSetup, consultez Propriétés de ICertSrvSetup.
ms.assetid: cb7f288b-30a0-4c3b-b7bc-3055166d2302
title: Méthodes de ICertSrvSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28274e1f59a4c229587f7e9f73222381ca89cff1a112ef7dc633f7a0c32dd434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407889"
---
# <a name="methods-of-icertsrvsetup"></a>Méthodes de ICertSrvSetup

Les méthodes suivantes sont définies par l’interface [**ICertSrvSetup**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetup) . Les méthodes d’accès à la propriété ne sont pas indiquées ici. Pour afficher les propriétés de **ICertSrvSetup**, consultez [Propriétés de ICertSrvSetup](properties-of-icertsrvsetup.md).



| Méthode                                                                         | Description                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAImportPFX**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-caimportpfx)                               | Importe un certificat d’autorité de certification et sa clé privée associée dans le magasin « LocalMachine ».                                                                                                                                          |
| [**GetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getcasetupproperty)                 | Obtient une valeur de propriété pour une configuration d’autorité de certification.                                                                                                                                                                                                             |
| [**GetExistingCACertificates**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getexistingcacertificates)   | Obtient la collection d’objets **CCertSrvSetupKeyInformation** qui représentent des certificats d’autorité de certification valides actuellement installés sur l’ordinateur.                                                                                                                  |
| [**GetHashAlgorithmList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-gethashalgorithmlist)             | Obtient la liste des algorithmes de hachage pris en charge par le [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) spécifié pour un algorithme de signature de clé asymétrique. |
| [**GetKeyLengthList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getkeylengthlist)                     | Obtient la liste des longueurs de clé prises en charge par le fournisseur de services de chiffrement spécifié.                                                                                                                                                                                              |
| [**GetPrivateKeyContainerList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprivatekeycontainerlist) | Obtient la liste des noms de conteneurs de clés stockés par le fournisseur de services de chiffrement spécifié pour les algorithmes de clé de signature asymétrique.                                                                                                                                                 |
| [**GetProviderNameList**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getprovidernamelist)               | Obtient la liste des fournisseurs de services de chiffrement qui fournissent des algorithmes de signature de clé asymétrique sur l’ordinateur.                                                                                                                                                                   |
| [**GetSupportedCATypes**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-getsupportedcatypes)               | Obtient les types d’autorités de certification qui peuvent être installés sur un ordinateur sous le contexte de l’appelant.                                                                                                                                                                       |
| [**InitializeDefaults**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-initializedefaults)                 | Initialise un objet **CCertSrvSetup** avec des valeurs par défaut pour permettre l’installation d’un rôle d’autorité de certification.                                                                                                                                                           |
| [**Installer**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-install)                                       | Installe un rôle d’autorité de certification comme configuré dans l’objet **CCertSrvSetup** .                                                                                                                                                                                         |
| [**IsPropertyEditable**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-ispropertyeditable)                 | Indique à l’appelant si une propriété spécifiée peut être modifiée.                                                                                                                                                                                       |
| [**PostUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-postuninstall)                           | N’est pas implémenté et est réservé à une utilisation ultérieure.                                                                                                                                                                                                        |
| [**PreUnInstall**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-preuninstall)                             | Enregistre temporairement les informations d’État spécifiques au rôle.                                                                                                                                                                                                        |
| [**SetCADistinguishedName**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcadistinguishedname)         | Définit un nom commun d’autorité de certification et un suffixe de nom unique facultatif.                                                                                                                                                                                          |
| [**SetCASetupProperty**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setcasetupproperty)                 | Définit une valeur de propriété pour une configuration d’autorité de certification.                                                                                                                                                                                                             |
| [**SetDatabaseInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setdatabaseinformation)         | Définit les informations relatives à la base de données pour le rôle d’autorité de certification.                                                                                                                                                                                                    |
| [**SetParentCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setparentcainformation)         | Définit les informations de l’autorité de certification parente pour une configuration d’autorité de certification secondaire.                                                                                                                                                                                        |
| [**SetWebCAInformation**](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetup-setwebcainformation)               | Définit les informations d’autorité de certification pour le rôle d’inscription par le Web de l’autorité de certification.                                                                                                                                                                                                   |



 

 

 
