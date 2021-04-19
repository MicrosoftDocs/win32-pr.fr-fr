---
description: Le stockage protégé fournit aux applications une interface permettant de stocker les données utilisateur qui doivent rester sécurisées ou exemptes de modifications.
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: PStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d291b911c351cce10827b7937c6a474b7c570
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544198"
---
# <a name="pstore"></a>PStore

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Le stockage protégé fournit aux applications une interface permettant de stocker les données utilisateur qui doivent rester sécurisées ou exemptes de modifications.

Les unités de données stockées sont appelées éléments. La structure et le contenu des données stockées sont opaques pour le système de stockage protégé. L’accès aux éléments est soumis à une confirmation selon un style de sécurité défini par l’utilisateur, qui spécifie la confirmation requise pour accéder aux données, par exemple si un mot de passe est requis. En outre, l’accès aux éléments est soumis à un ensemble de règles d’accès. Il existe une règle d’accès pour chaque mode d’accès : par exemple, en lecture/écriture. Les ensembles de règles d’accès sont composés de clauses d’accès. Deux types de clauses d’accès sont actuellement pris en charge : Authenticode et vérification binaire de l’appelant. Généralement au moment de l’installation de l’application, un mécanisme permet à une nouvelle application de demander à l’utilisateur d’accéder à des éléments qui ont pu être créés précédemment par une autre application.

Les éléments sont identifiés de manière unique par la combinaison d’une clé, d’un type, d’un sous-type et d’un nom. La clé est une constante qui spécifie si l’élément est global pour cet ordinateur ou s’il est associé uniquement à cet utilisateur. Le nom est une chaîne, généralement choisie par l’utilisateur. Le type et le sous-type sont des **GUID**, généralement spécifiés par l’application. Des informations supplémentaires sur les types et les sous-types sont conservées dans le registre système et incluent des attributs tels que le nom d’affichage et les indicateurs d’interface utilisateur. Pour les sous-types, le type parent est fixe et inclus dans le registre système en tant qu’attribut. Les éléments de groupe de types sont utilisés à des fins courantes : par exemple, le paiement ou l’identification. Les éléments de groupe de sous-type partagent un format de données commun.

## <a name="in-this-section"></a>Dans cette section

-   [**IEnumPStoreItems**](ienumpstoreitems.md)
-   [**IEnumPStoreProviders**](ienumpstoreproviders.md)
-   [**IEnumPStoreTypes**](ienumpstoretypes.md)
-   [**IPStore**](ipstore.md)
-   [**PStoreCreateInstance**](pstorecreateinstance.md)
-   [**PStoreEnumProviders**](pstoreenumproviders.md)
-   [**Constantes PStore**](pstore-constants.md)
-   [**Types PStore**](pstore-types.md)

 

 
