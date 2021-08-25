---
title: Attribut Package-Flags
description: Champ de champ binaire qui contient les indicateurs d’état de déploiement pour une application.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Schéma AD d’attribut Package-Flags
- Schéma AD de l’attribut packageFlags
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd6965b5c39603032bdb673df10026b0eed2a5d5ae838aeb094013d9a5e95dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923939"
---
# <a name="package-flags-attribute"></a>Attribut Package-Flags

Champ de champ binaire qui contient les indicateurs d’état de déploiement pour une application.

Cet attribut peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.

| Valeur                 | Description                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | La version non gérée de cette application doit être désinstallée avant d’être assignée. **Windows XP avec SP1 et versions ultérieures :** Cet indicateur n’est pas pris en charge.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Il s’agit d’une application publiée.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | ce package a été déployé après la version bêta 3 de Windows 2000.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Cette application peut être installée avec la fonctionnalité **Ajout/suppression de programmes** du panneau de configuration.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Cette application peut être installée automatiquement à la demande.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Cette application est orpheline. Une application publiée peut devenir orpheline si l’administrateur supprime l’application de la liste des applications pouvant être déployées.<br/>                                                                                                                                    |
| 0x00000100<br/> | Cette application doit être traitée comme étant désinstallée.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Cette application est uniquement disponible en tant que pilote.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Il s’agit d’une application affectée. Une application affectée ne peut pas être entièrement supprimée par l’utilisateur. Si l’utilisateur tente de désinstaller l’application à l’aide de la fonctionnalité **Ajout/suppression de programmes** du panneau de configuration, l’application est de nouveau publiée sur l’ordinateur une fois la suppression terminée.<br/> |
| 0x00000800<br/> | Cette application est orpheline lorsque la stratégie est supprimée. Si l’administrateur supprime la stratégie associée à cette application, l’administrateur ne contrôlera plus le déploiement de l’application, mais l’application installée continuera à fonctionner.<br/>                          |
| 0x00001000<br/> | Cette application est désinstallée lors de la suppression de la stratégie de déploiement.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Une installation complète des applications affectées par l’utilisateur est exécutée.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Les versions antérieures de cette application doivent être mises à niveau vers cette version.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Ce package ne prend en charge qu’une interface utilisateur minimale avec une barre de progression pour le processus d’installation.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | il s’agit d’un package pour les versions 32 bits de Windows qui ne doivent pas être exécutées sur Windows XP Professional édition x64 ou sur les versions 64 bits de Windows Server 2003.<br/>                                                                                                                                      |
| 0x00020000<br/> | Ce package convient à n’importe quel langage.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Ce package a des mises à niveau.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Ce package a une interface utilisateur complète pour le processus d’installation.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | Les classes de cette application sont conservées lors d’une opération de redéploiement si l’application est redéployée dans un changement de nom de domaine.<br/>                                                                                                                                                                       |



 



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| LDAP-Display-Name | packageFlags                         |
| Taille              | \-                                   |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-ID-GUID    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Syntaxe            | [**Énumération**](s-enumeration.md) |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Vrai                                                             |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Vrai                                                             |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Vrai                                                             |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Vrai                                                             |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Vrai                                                             |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrée | Valeur |
|------------------------|------------------------------------------------------------------|
| ID de lien                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Faux                                                            |
| Est de valeur unique       | Vrai                                                             |
| Est indexé             | Vrai                                                             |
| Dans le catalogue global      | Faux                                                            |
| Descripteur de sécurité NT | O :BAG : BAD : S :                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classes utilisées dans        | [**Inscription de packages**](c-packageregistration.md)<br/> |



 

 





