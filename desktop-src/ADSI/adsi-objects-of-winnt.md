---
title: Objets ADSI de Winnt
description: Le fournisseur Winnt ADSI implémente les objets COM suivants pour prendre en charge les fonctionnalités et les services de différentes interfaces ADSI.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- ADSI, fournisseur de service WinNT, objets ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f3d2cb845e7fa6c754198abbb9a274987f69a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467386"
---
# <a name="adsi-objects-of-winnt"></a>Objets ADSI de Winnt

Le fournisseur Winnt ADSI implémente les objets COM suivants pour prendre en charge les fonctionnalités et les services de différentes interfaces ADSI.




| Objet ADSI | Description | Interfaces prises en charge | 
|-------------|-------------|----------------------|
| <strong>Classe</strong> | Objet ADSI qui représente une définition de classe. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt></dl> | 
| <strong>Ordinateur</strong> | Objet ADSI qui représente un ordinateur. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Domaine</strong> | Objet ADSI qui représente un domaine sur le réseau. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileService</strong> | Objet ADSI qui représente un service de fichiers. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FileShare</strong> | Objet ADSI qui représente un partage de fichiers. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWFileService</strong> | Objet ADSI qui représente un service de fichiers. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>FPNWFileShare</strong> | Objet ADSI qui représente un partage de fichiers. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResource</strong> | Objet ADSI qui représente une ressource. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWResourcesCollection</strong> | Objet ADSI qui représente une collection de ressources. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>FPNWSession</strong> | Objet ADSI qui représente une session. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>FPNWSessionsCollection</strong> | Objet ADSI qui représente une collection de sessions. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Groupe</strong> | Objet ADSI qui représente un groupe. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl><blockquote>[!Note]<br />GetInfo ne peut pas être utilisé pour les groupes qui contiennent des membres qui sont des principaux de sécurité wellKnown dans l’étendue Winnt.</blockquote><br /> | 
| <strong>GroupCollection</strong> | Objet ADSI qui représente une collection de groupes. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>LocalGroup</strong> | Objet ADSI qui représente un groupe local. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>LocalgroupCollection</strong> | Objet ADSI qui représente une collection de groupes locaux. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt></dl> | 
| <strong>Espace de noms</strong> | Objet ADSI qui représente l’espace de noms Winnt. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt></dl> | 
| <strong>PrintJob</strong> | Objet ADSI qui représente un travail d’impression. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>PrintJobsCollection</strong> | Objet ADSI qui représente une collection de travaux d’impression. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>PrintQueue</strong> | Objet ADSI qui représente une file d’attente à l’impression. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Propriété</strong> | Objet ADSI qui représente une définition d’attribut. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt></dl> | 
| <strong>Ressource</strong> | Objet ADSI qui représente une ressource. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>ResourcesCollection</strong> | Objet ADSI qui représente une collection de ressources. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Schéma</strong> | Objet ADSI qui représente le conteneur de schéma. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt></dl> | 
| <strong>Service</strong> | Objet ADSI qui représente un service. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>Session</strong> | Objet ADSI qui représente une session. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>SessionsCollection</strong> | Objet ADSI qui représente une collection de sessions. | <a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a> | 
| <strong>Syntaxe</strong> | Objet ADSI qui représente la syntaxe d’un attribut. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt></dl> | 
| <strong>Utilisateur</strong> | Objet ADSI qui représente un compte d’utilisateur. | <dl><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt><dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt></dl> | 
| <strong>UserGroupCollection</strong> | Objet ADSI qui représente une collection de groupes d’utilisateurs. | <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a> | 




 

 

 





