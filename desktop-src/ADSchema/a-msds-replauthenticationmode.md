---
title: attribut ms-DS-REPL-authentication-mode
description: L’attribut ms-DS-REPL-authentication-mode est utilisé pour spécifier la méthode d’authentification utilisée pour authentifier les partenaires de réplication.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut ms-DS-REPL-authentication-mode
- Schéma Active Directory de l’attribut msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff624a9b7a1d1f678c748f79d3193b0b4b287026de1a669896c3e25d69f27ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803539"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>attribut ms-DS-REPL-authentication-mode

L’attribut **ms-DS-REPL-authentication-mode** est utilisé pour spécifier la méthode d’authentification utilisée pour authentifier les partenaires de réplication. Cet attribut s’applique à la partition de configuration d’une instance ADAM.

Les valeurs suivantes sont les valeurs possibles pour cet attribut.

| Valeur        | Méthode d'authentification                          | Description                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Authentification directe négociée<br/>             | Toutes les instances ADAM dans le jeu de configuration utilisent un nom de compte et un mot de passe identiques en tant que compte de service ADAM.<br/>                                                 |
| 1<br/> | Negotiated<br/>                          | L'authentification Kerberos (à l'aide de noms principaux de service) est tentée en premier. Si elle échoue, l'authentification NTLM est tentée. Si NTLM échoue, les instances ADAM ne seront pas répliquées.<br/> |
| 2<br/> | Authentification mutuelle avec Kerberos<br/> | Authentification Kerberos, utilisation de noms principaux de services (SPN), obligatoire. Si l’authentification Kerberos échoue, les instances ADAM ne seront pas répliquées.<br/>                |



 

Le tableau suivant contient les identificateurs programmatiques pour les valeurs de cet attribut.

| Valeur        | Identificateur (à partir de ntdsapi. h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **\_ \_ \_ relais en mode d’authentification REPL \_ \_ \_ par négociation**<br/> |
| 1<br/> | **\_négociation du \_ mode d’authentification REPL par Adam \_ \_**<br/>                |
| 2<br/> | **\_ \_ authentification mutuelle du mode d’authentification REPL \_ \_ \_ \_ requise**<br/>   |



 



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-REPL-authentication-mode       |
| LDAP-Display-Name | msDS-ReplAuthenticationMode          |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-ID-GUID    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|-----------------------------------------------------|
| ID de lien                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Faux                                               |
| Est de valeur unique       | Vrai                                                |
| Est indexé             | Faux                                               |
| Dans le catalogue global      | Faux                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes utilisées dans        | [**Configuration**](c-configuration.md)<br/> |



 

 





