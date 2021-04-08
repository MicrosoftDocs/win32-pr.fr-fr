---
title: Prise en charge des langages de programmation
description: Vous pouvez écrire des applications clientes ADSI dans de nombreux langages.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839149"
---
# <a name="programming-language-support"></a>Prise en charge des langages de programmation

Vous pouvez écrire des applications clientes ADSI dans de nombreux langages. Pour la majorité des tâches d’administration, ADSI définit des interfaces et des objets accessibles à partir de langages conformes à Automation. Par exemple, le système de développement Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript) et Java, ainsi que des langages plus performants en termes de performances et d’efficacité, comme C et C++.

L’intégration lisse avec les pages de Active Server et VBScript facilite l’écriture d’applications Internet qui accèdent aux services d’annuaire. Pour l’intégration avec les applications OLE DB, ADSI fournit un fournisseur OLE DB en prenant en charge un sous-ensemble des interfaces de requête OLE DB. Le fournisseur OLE DB prend en charge l’accès en lecture seule aux Active Directory.

Pour les applications Internet, l’utilisation de scripts dans les fichiers Active Server page (ASP) peut créer et manipuler des objets ADSI sur le serveur et afficher les résultats dans une page Web. Dans Microsoft Management Console, les composants logiciels enfichables d’administration de service d’annuaire peuvent utiliser ADSI pour rechercher des services d’annuaire intéressants. En bref, Active Directory interfaces de service peuvent fournir l’accès à un ensemble vaste et diversifié de services d’annuaire, y compris ceux qui n’ont pas encore été générés.

Pour accéder aux structures qui utilisent des API traditionnelles, l’architecture ADSI définit des interfaces de bas niveau qui ne prennent pas en charge l’Automation qui sont accessibles à partir de langages tels que C et C++. Ces interfaces sont peu plus petites que les wrappers COM pour les protocoles réseau vers un service d’annuaire.

L’écriture de code dans les interfaces publiées permet à votre application d’accéder aux services d’annuaire pour tous les fournisseurs ADSI installés et d’intégrer les données résultantes. Avec peu ou pas de modifications à votre code, votre application peut continuer à accéder à des services d’annuaire supplémentaires sur votre réseau à mesure que de nouveaux fournisseurs ADSI sont installés.

La figure suivante illustre l’intégration d’ADSI dans un environnement d’application. Que l’application soit écrite en Visual Basic, C/C++, VBScript, le système de développement Microsoft JScript ou en tant qu’application Web à l’aide de Active Server pages, les interfaces de service Active Directory fournissent un accès propre et facile aux services d’annuaire sous-jacents sans avoir à utiliser les API réseau natives.

![prise en charge d’ADSI pour les langages de programmation](images/ds2layr.png)

Comme indiqué dans la figure précédente, les clients qui ne prennent pas en charge Automation ont accès à toutes les interfaces ADSI, y compris les interfaces COM pures avec la Convention d’affectation de noms **IDirectoryXXX** et les interfaces com Automation avec la Convention d’affectation de noms **IADsXXX**. Étant donné que les clients demandent principalement des informations à partir des services d’annuaire, le modèle de requête flexible ADSI via OLE DB et [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) est efficace.

 

 




