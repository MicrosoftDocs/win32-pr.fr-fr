---
title: Utilisation de l’extension ADSI pour Services Bureau à distance Configuration utilisateur
description: L’administration des propriétés utilisateur spécifiques à Services Bureau à distance est possible en utilisant les méthodes implémentées par l’extension ADSI (Active Directory Service Interfaces), qui est empaquetée avec la bibliothèque de liens dynamiques Tsuserex.dll.
ms.assetid: f6355730-9686-4446-b118-630562548fc9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance à l’aide de l’extension ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe63a725531c21b64ed0ac10abdeb4f710465532ab95f7c416c88f6142f1d55e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423689"
---
# <a name="using-the-adsi-extension-for-remote-desktop-services-user-configuration"></a>Utilisation de l’extension ADSI pour Services Bureau à distance Configuration utilisateur

L’extension ADSI (Active Directory Service Interfaces) pour Services Bureau à distance Configuration utilisateur est une bibliothèque qui est empaquetée à l’aide de la bibliothèque de liens dynamiques Tsuserex.dll. L’administration des propriétés utilisateur spécifiques à Services Bureau à distance est possible à l’aide des méthodes implémentées par l’extension. Les méthodes permettent de configurer les propriétés qui sont disponibles dans l’interface d’extension pour les utilisateurs Services Bureau à distance.

L’extension ADSI pour Services Bureau à distance Configuration utilisateur prend en charge l’examen et la manipulation de Services Bureau à distance propriétés utilisateur stockées dans la base de données du service d’annuaire. L’extension prend également en charge la configuration des propriétés utilisateur stockées dans le Active Directory, par le biais de l’API LDAP (Lightweight Directory Access Protocol).

Le fournisseur implémente les méthodes suivantes :

-   [**IADs :: obten**](/windows/desktop/api/iads/nf-iads-iads-get). Cette méthode recherche une propriété ou un ensemble de propriétés spécifiques sur une instance de la classe.
-   [**IADs ::P ut**](/windows/desktop/api/iads/nf-iads-iads-put). Cette méthode Configure une propriété spécifique ou un ensemble de propriétés sur une instance de la classe.

Pour obtenir la liste des propriétés Services Bureau à distance utilisateur spécifiques que vous pouvez configurer, consultez la [référence de l’extension ADSI pour services Bureau à distance Configuration utilisateur](reference-for-the-adsi-extension-for-terminal-services-user-configuration.md) .

Pour plus d’informations sur l’accès et la modification des attributs avec ADSI, consultez [accès et manipulation des données avec ADSI](/windows/desktop/ADSI/accessing-and-manipulating-data-with-adsi).

Pour plus d’informations sur l’utilisation des conventions d’affectation de noms ADSI et des chaînes AdsPath, consultez les informations sur les [fournisseurs de services ADSI](/windows/desktop/ADSI/adsi-system-providers) individuels dans la documentation du kit de développement logiciel (SDK) de la plate-forme [Interfaces de service Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) .

 

 