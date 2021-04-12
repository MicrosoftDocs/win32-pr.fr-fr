---
title: Attribut de descripteur de sécurité NT
description: Descripteur de sécurité Windows NT pour l’objet de schéma. Un descripteur de sécurité est une structure de données qui contient des informations de sécurité sur un objet, telles que la propriété et les autorisations de l’objet.
ms.assetid: 3a17b584-97ea-441c-846e-3031aea171b2
ms.tgt_platform: multiple
keywords:
- Schéma AD de l’attribut de descripteur de sécurité NT
- Schéma AD de l’attribut nTSecurityDescriptor
topic_type:
- apiref
api_name:
- NT-Security-Descriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e951e28ce97b04380609774baf57e4c6bf8c545
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519713"
---
# <a name="nt-security-descriptor-attribute"></a>Attribut de descripteur de sécurité NT

Descripteur de sécurité Windows NT pour l’objet de schéma. Un descripteur de sécurité est une structure de données qui contient des informations de sécurité sur un objet, telles que la propriété et les autorisations de l’objet.

Pour plus d’informations sur le format de cette valeur, consultez [format de chaîne du descripteur de sécurité (Windows)](https://msdn.microsoft.com/library(d=robot)/aa379570(d=robot,l=en-us,v=vs.85).aspx).



| Entrée | Valeur |
|-------------------|-----------------------------------------------------|
| CN                | Descripteur de sécurité NT                              |
| LDAP-Display-Name | nTSecurityDescriptor                                |
| Taille              | \-                                                  |
| Mettre à jour le privilège  | \-                                                  |
| Fréquence des mises à jour  | \-                                                  |
| Attribute-Id      | 1.2.840.113556.1.2.281                              |
| System-ID-GUID    | bf9679e3-0de6-11d0-a285-00aa003049e2                |
| Syntaxe            | [**String(NT-Sec-Desc)**](s-string-nt-sec-desc.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Faux                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                               |
| Est indexé             | Faux                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x00000012                                                                                                                                         |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Faux                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                               |
| Est indexé             | Faux                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                           |
| MAPI-Id                | 0x8013                                                                                       |
| System-Only            | Faux                                                                                        |
| Est de valeur unique       | Vrai                                                                                         |
| Est indexé             | Faux                                                                                        |
| Dans le catalogue global      | Vrai                                                                                         |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                 |
| Range-Lower            | 0                                                                                            |
| Range-Upper            | 132096                                                                                       |
| Search-Flags           | 0x00000008                                                                                   |
| System-Flags           | 0x0000001A                                                                                   |
| Classes utilisées dans        | [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Faux                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                               |
| Est indexé             | Faux                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Faux                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                               |
| Est indexé             | Faux                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Faux                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                               |
| Est indexé             | Faux                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| ID de lien                | \-                                                                                                                                                 |
| MAPI-Id                | 0x8013                                                                                                                                             |
| System-Only            | Faux                                                                                                                                              |
| Est de valeur unique       | Vrai                                                                                                                                               |
| Est indexé             | Faux                                                                                                                                              |
| Dans le catalogue global      | Vrai                                                                                                                                               |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                  |
| Range-Upper            | 132096                                                                                                                                             |
| Search-Flags           | 0x00000008                                                                                                                                         |
| System-Flags           | 0x0000001A                                                                                                                                         |
| Classes utilisées dans        | [**Sam-domaine-base**](c-samdomainbase.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |



 

 





