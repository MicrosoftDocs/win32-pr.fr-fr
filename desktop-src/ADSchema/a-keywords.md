---
title: Attribut Keywords
description: Liste de mots clés qui peuvent être utilisés pour localiser un point de connexion donné.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Attribut des mots clés-schéma Active Directory
- attribut des mots clés-schéma Active Directory
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5c1fba475505ee03cda4813f90a28d1c91fb69
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744812"
---
# <a name="keywords-attribute"></a>Attribut Keywords

Liste de mots clés qui peuvent être utilisés pour localiser un point de connexion donné.



| Entrée | Valeur |
|-------------------|---------------------------------------------|
| CN                | Mots clés                                    |
| LDAP-Display-Name | mots clés                                    |
| Taille              | \-                                          |
| Mettre à jour le privilège  | \-                                          |
| Fréquence des mises à jour  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-ID-GUID    | bf967993-0de6-11d0-a285-00aa003049e2        |
| Syntaxe            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|----------------------------------------------------------|
| ID de lien                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Faux                                                    |
| Est de valeur unique       | Faux                                                    |
| Est indexé             | Vrai                                                     |
| Dans le catalogue global      | Vrai                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| Classes utilisées dans        | [**Point de connexion**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Faux                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                   |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Version de l’application**](c-applicationversion.md)<br/> [**Point de connexion**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-données**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | Faux                                                                                                                    |
| Est de valeur unique       | Faux                                                                                                                    |
| Est indexé             | Vrai                                                                                                                     |
| Dans le catalogue global      | Vrai                                                                                                                     |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| Classes utilisées dans        | [**ms-DS-Service-Connection-point-publication-service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Faux                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                   |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Version de l’application**](c-applicationversion.md)<br/> [**Point de connexion**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-données**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Faux                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                   |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Version de l’application**](c-applicationversion.md)<br/> [**Point de connexion**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-données**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Faux                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                   |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Version de l’application**](c-applicationversion.md)<br/> [**Point de connexion**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-données**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Faux                                                                                                                                                                                                                                                                                   |
| Est de valeur unique       | Faux                                                                                                                                                                                                                                                                                   |
| Est indexé             | Vrai                                                                                                                                                                                                                                                                                    |
| Dans le catalogue global      | Vrai                                                                                                                                                                                                                                                                                    |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Classes utilisées dans        | [**Version de l’application**](c-applicationversion.md)<br/> [**Point de connexion**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**ms-DS-App-configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-données**](c-msds-appdata.md)<br/> |



 

 





