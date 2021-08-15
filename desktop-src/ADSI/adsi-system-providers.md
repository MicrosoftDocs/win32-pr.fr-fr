---
title: Fournisseurs de services ADSI
description: Cette rubrique donne une vue d’ensemble des fournisseurs de services ADSI fournis sur le serveur.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, fournisseurs de services
- Fournisseurs de services ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66b90aad4e9fa1a6cf6a2229910257f018a411aa7b11b9accca6fcf96dce39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962199"
---
# <a name="adsi-service-providers"></a>Fournisseurs de services ADSI

ADSI comprend les fournisseurs de services listés dans le tableau suivant.



| Fournisseur de services | Description                                                                                | Informations supplémentaires                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implémentation de l’espace de noms compatible avec le protocole Lightweight Directory Access.<br/> | [Fournisseur LDAP ADSI](adsi-ldap-provider.md)<br/>   |
| NT<br/> | Implémentation de l’espace de noms compatible avec Windows.<br/>                               | [Fournisseur WinNT ADSI](adsi-winnt-provider.md)<br/> |



 

D’autres fournisseurs de services sont inclus dans le cadre de produits autres qu’ADSI. Les fournisseurs de services ADSI implémentés par Microsoft sont les suivants.



| Fournisseur de services | Informations supplémentaires                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Architecture du fournisseur ADSI IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Les méthodes et méthodes de propriété exposées par les interfaces ADSI ne sont pas prises en charge par chaque fournisseur de services. Étant donné que les différents services d’annuaire varient selon les types d’objets et de propriétés stockés, utilisent des protocoles différents et l’authentification, ADSI est conçu pour fonctionner de manière transparente avec les fournisseurs de services pris en charge. Par conséquent, il existe des interfaces, des méthodes et des méthodes de propriété qui fonctionnent avec un fournisseur de services, tel que LDAP, qui peut ne pas fonctionner sur un autre, tel que Winnt.

Cette section contient des informations spécifiques au fournisseur, telles que le format ADsPath, une liste des objets ADSI utilisés pour ce fournisseur de services, ainsi que des informations sur le type de données et la syntaxe pour les fournisseurs de services inclus avec ADSI. Il existe également une description résumée des interfaces ADSI prises en charge par chaque fournisseur inclus dans ADSI.

Dans ADSI, différents fournisseurs sont associés à différentes dll. Le fournisseur LDAP est associé à Adsldp.dll, Adsldpc.dll et Adsmsext.dll. Le fournisseur Winnt est associé à Adsnt.dll. Le fournisseur de routeur est associé à Activeds.dll.

> [!Note]  
> Ne partez pas du principe que les fournisseurs ADSI par défaut sont thread-safe. Les développeurs d’applications multithread doivent coordonner l’accès entre les threads par le biais de l’utilisation appropriée d’objets de synchronisation tels que les sémaphores, les mutex, les sections critiques, etc.

 

Pour plus d’informations sur les fournisseurs de services [](adsi-router.md) ADSI, consultez [prise en charge du routeur ADSI et du fournisseur d’interfaces ADSI](provider-support-of-adsi-interfaces.md).

 

