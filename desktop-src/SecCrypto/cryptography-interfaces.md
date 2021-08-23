---
description: Répertorie les interfaces fournies par CryptoAPI.
ms.assetid: f94f0264-78b8-4a28-9d3a-dda55db29897
title: Interfaces de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5937dce6da8ffa3396c885d00c895b845de9889c2688c6daef4eba5db0beb90b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876099"
---
# <a name="cryptography-interfaces"></a>Interfaces de chiffrement

Les interfaces de chiffrement sont classées en fonction de l’utilisation comme suit :

-   [Interfaces d’exportation du moteur du serveur](#server-engine-export-interfaces)
-   [Interfaces d’importation du moteur du serveur](#server-engine-import-interfaces)
-   [Interfaces d’encodage](#encoding-interfaces)
-   [Interfaces d’inscription de certificats](#certificate-enrollment-interfaces)
-   [Interfaces d’interopérabilité CAPICOM](#capicom-interoperability-interfaces)

## <a name="server-engine-export-interfaces"></a>Interfaces d’exportation du moteur du serveur

La rubrique de référence suivante décrit les interfaces qui sont exportées par le moteur de serveur et qui sont appelées par des objets externes.



| Interface                                                                | Description                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin)                                         | Utilisé par les programmes d’administration pour gérer les demandes, les certificats et les révocations.                                                                                                                                                              |
| [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2)                                       | Utilisé par les programmes d’administration pour gérer les demandes, les certificats et les révocations. Remplace [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin).                                                                                                                 |
| [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig)                                       | Utilisé par les clients pour obtenir des informations sur les serveurs disponibles.                                                                                                                                                                                 |
| [**ICertConfig2**](/windows/desktop/api/Certcli/nn-certcli-icertconfig2)                                     | Utilisé par les clients pour obtenir des informations sur les serveurs disponibles. Remplace [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig).                                                                                                                                  |
| [**ICertGetConfig**](/windows/desktop/api/Certcli/nn-certcli-icertgetconfig)                                 | Fournit les fonctionnalités permettant de récupérer les données de configuration publiques (spécifiées lors de l’installation du client) pour un serveur de [*services de certificats*](../secgloss/c-gly.md) .                |
| [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest)                                     | Permet d’envoyer une requête au serveur et d’obtenir les résultats de la demande.                                                                                                                                                                        |
| [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2)                                   | Permet d’envoyer une requête au serveur et d’obtenir les résultats de la demande. Remplace [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest).                                                                                                                       |
| [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit)                               | Utilisé par les [modules de sortie](exit-modules.md) pour obtenir les propriétés du certificat et de la demande.                                                                                                                                                             |
| [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy)                           | Utilisé par le [module de stratégie](policy-modules.md) pour obtenir et définir des propriétés de certificat et de demande.                                                                                                                                              |
| [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview)                                           | Utilisé par les clients pour [afficher la base de données des services de certificats](viewing-the-certificate-services-database.md).                                                                                                                                 |
| [**ICertView2**](/windows/desktop/api/Certview/nn-certview-icertview2)                                         | Utilisé par les clients pour afficher la base de données des services de certificats. Remplace [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview).                                                                                                                                       |
| [**IEnumCERTVIEWATTRIBUTE**](/windows/desktop/api/Certview/nn-certview-ienumcertviewattribute)                 | Utilisé par les clients pour accéder aux attributs de certificat d’une ligne dans la vue des services de certificats.                                                                                                                                                |
| [**IEnumCERTVIEWCOLUMN**](/windows/desktop/api/Certview/nn-certview-ienumcertviewcolumn)                       | Utilisé par les clients pour accéder aux colonnes de données d’une ligne dans la vue des services de certificats.                                                                                                                                                           |
| [**IEnumCERTVIEWEXTENSION**](/windows/desktop/api/Certview/nn-certview-ienumcertviewextension)                 | Utilisé par les clients pour accéder aux données d’extension de certificat pour une ligne dans la vue des services de certificats.                                                                                                                                            |
| [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow)                             | Utilisé par les clients pour énumérer les lignes de la vue des services de certificats.                                                                                                                                                                         |
| [**IOCSPAdmin**](/windows/desktop/api/certadm/nn-certadm-iocspadmin)                                         | Utilisé par les programmes d’administration pour configurer les serveurs répondeurs OCSP (Online Certificate Status Protocol).                                                                                                                                       |
| [**IOCSPCAConfiguration**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfiguration)                     | Fournit les fonctionnalités permettant de configurer un service de répondeur OCSP pour gérer les demandes d’État pour une [*autorité de certification*](../secgloss/c-gly.md) (ca) spécifique.<br/> |
| [**IOCSPCAConfigurationCollection**](/windows/desktop/api/Certadm/nn-certadm-iocspcaconfigurationcollection) | Fournit des fonctionnalités permettant de gérer les configurations de l’autorité de certification pour lesquelles un service de répondeur OCSP peut traiter les demandes.                                                                                                                                 |
| [**IOCSPProperty**](/windows/desktop/api/Certadm/nn-certadm-iocspproperty)                                   | Fournit les fonctionnalités permettant de configurer un attribut de serveur répondeur OCSP.                                                                                                                                                                         |
| [**IOCSPPropertyCollection**](/windows/desktop/api/Certadm/nn-certadm-iocsppropertycollection)               | Utilisé par les programmes d’administration pour gérer les attributs du serveur répondeur OCSP.                                                                                                                                                                     |



 

## <a name="server-engine-import-interfaces"></a>Interfaces d’importation du moteur du serveur

Les rubriques de référence suivantes décrivent les interfaces qui sont importées par le moteur serveur.



| Interface                                      | Description                                                                                                                            |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit)                 | Exporté par les modules de sortie. Utilisé par le moteur du serveur pour fournir des certificats et des informations de révocation finalisés.                       |
| [**ICertExit2**](/windows/desktop/api/Certexit/nn-certexit-icertexit2)               | Ajoute la méthode [**GetManageModule**](/windows/desktop/api/Certexit/nf-certexit-icertexit2-getmanagemodule) à [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit).                               |
| [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) | Exporté par les modules de stratégie ou de sortie. Permet d’afficher des informations de module ou d’afficher une interface utilisateur pour la configuration du module. |
| [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy)             | Exporté par le module de stratégie. Utilisé par le moteur du serveur pour vérifier les demandes et obtenir les propriétés des certificats.                        |
| [**ICertPolicy2**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy2)           | Ajoute la méthode [**GetManageModule**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy2-getmanagemodule) à [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy).                         |



 

## <a name="encoding-interfaces"></a>Interfaces d’encodage

Les rubriques de référence suivantes décrivent les interfaces qui peuvent être exportées par les [gestionnaires d’extension](writing-custom-extension-handlers.md) et qui sont importées par le module de stratégie.



| Interface                                                | Description                                                                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname)         | Utilisé par le [module de stratégie](policy-modules.md) pour gérer d’autres extensions de noms.                                                                                                                                                          |
| [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring)     | Utilisé par le module de stratégie pour gérer les chaînes de bits utilisées dans les extensions de certificat.                                                                                                                                                               |
| [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo) | Utilisé par le module de stratégie pour gérer les tableaux d’informations de distribution de [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL) utilisés dans les extensions de certificat. |
| [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray)     | Utilisé par le module de stratégie pour gérer les tableaux de **dates** utilisés dans les extensions de certificat.                                                                                                                                                           |
| [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)     | Utilisé par le module de stratégie pour gérer les tableaux **longs** utilisés dans les extensions de certificat.                                                                                                                                                           |
| [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray) | Utilisé par le module de stratégie pour gérer les tableaux de **chaînes** utilisés dans les extensions de certificat.                                                                                                                                                         |



 

## <a name="certificate-enrollment-interfaces"></a>Interfaces d’inscription de certificats

Cette section décrit les objets, méthodes et propriétés du contrôle d’inscription de certificats, ainsi que l’objet, les méthodes et les propriétés disponibles dans le contrôle d’inscription de carte à puce. Celles-ci incluent les interfaces suivantes.



| Interface                                                                                  | Description                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll)                                                               | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. Il vous intéresse principalement si vous n’utilisez pas Automation.                                                                        |
| [**ICEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll2)                                                             | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. Il vous intéresse principalement si vous n’utilisez pas Automation.                                                                        |
| [**ICEnroll3**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll3)                                                             | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. Il vous intéresse principalement si vous n’utilisez pas Automation.                                                                        |
| [**ICertificateEnrollmentPolicyServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentpolicyserversetup) | Représente le service Web stratégie d’inscription de certificats (CEP) dans Active Directory Services de certificats (ADCS). Le service permet aux utilisateurs et aux ordinateurs d’obtenir des informations sur la stratégie d’inscription de certificats. |
| [**ICertificateEnrollmentServerSetup**](/windows/desktop/api/Casetup/nn-casetup-icertificateenrollmentserversetup)             | Représente le service Web Inscription de certificats (ces) dans ADCS. Le service permet aux utilisateurs et aux ordinateurs de s’inscrire pour et de renouveler des certificats.                                                               |
| [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4)                                                             | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. Il vous intéresse principalement si vous n’utilisez pas Automation.                                                                        |
| [**IEnroll**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll)                                                                 | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. L’interface est principalement intéressante si vous n’utilisez pas Automation.                                                             |
| [**IEnroll2**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll2)                                                               | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. L’interface est principalement intéressante si vous n’utilisez pas Automation.                                                             |
| [**IEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-ienroll4)                                                               | Une des nombreuses interfaces qui représentent le contrôle d’inscription de certificat. L’interface est principalement intéressante si vous n’utilisez pas Automation.                                                             |
| [**ISCrdEnr**](iscrdenr.md)                                                               | Représente le contrôle d’inscription de carte à puce. Il vous intéresse principalement si vous n’utilisez pas Automation.                                                                                                       |



 

## <a name="capicom-interoperability-interfaces"></a>Interfaces d’interopérabilité CAPICOM

Les rubriques de référence suivantes décrivent les interfaces qui permettent aux dérivations de fonctionner conjointement avec CAPICOM 2,0.



| Interface                              | Description                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fournit l’accès au contexte d’un objet de [**certificat**](certificate.md) CAPICOM X. 509v3. Ce contexte permet d’utiliser le certificat CAPICOM dans d’autres dérivations de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fournit l’accès au contexte d’un objet de [**magasin**](store.md) CAPICOM. Ce contexte permet d’utiliser le magasin de certificats CAPICOM dans d’autres dérivations de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fournit l’accès au contexte d’un objet de [**chaîne**](chain.md) CAPICOM. Ce contexte autorise l’utilisation de la chaîne d’approbation de certificat CAPICOM dans d’autres dérivations de CryptoAPI.         |



 

 

 
