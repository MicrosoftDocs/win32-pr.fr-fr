---
description: Répertorie les types de données utilisés par les dll d’attachement de configuration de sécurité et leurs fonctions de prise en charge.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Types de données de gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095833"
---
# <a name="security-management-data-types"></a>Types de données de gestion de la sécurité

Les types de données de gestion de la sécurité sont les suivants :

-   [Types de données de pièce jointe](#attachment-data-types)
-   [Types de données de la stratégie LSA](#lsa-policy-data-types)

## <a name="attachment-data-types"></a>Types de données de pièce jointe

Les types de données suivants sont utilisés par les dll de la configuration de sécurité jointes et leurs fonctions de prise en charge.



| Type de données                                                    | Description                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexte d’énumération SCE \_**](sce-enumeration-context.md) | Utilisé par la fonction [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) pour naviguer dans la base de données de sécurité.                                                                                                                                              |
| [**\_handle SCE**](sce-handle.md)                            | Utilisé par [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) et [**PFSCE \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) pour transmettre des informations entre la pièce jointe et la base de données de sécurité.                                                                                 |
| [**SCESTATUS**](scestatus.md)                               | Le type de données est utilisé par l’API Set de l’outil de configuration de la sécurité pour retourner des informations sur les résultats d’un appel de fonction.                                                                                                                                    |
| [**\_handle SCESVC**](scesvc-handle.md)                      | Utilisé par les méthodes des interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) et [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) pour passer des informations entre le composant logiciel enfichable Configuration de la sécurité et l’extension du composant logiciel enfichable. |
| [**\_type d’informations SCESVC \_**](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | L’énumération est utilisée par les informations de [**\_ requête \_ PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) et [**PFSCE \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) pour indiquer le type d’informations demandées ou transmises à la base de données de sécurité.                                                 |



 

## <a name="lsa-policy-data-types"></a>Types de données de la stratégie LSA

Les types de données suivants sont utilisés par les fonctions de gestion de la stratégie LSA.



| Type de données                                                  | Description                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_handle d’énumération LSA \_**](lsa-enumeration-handle.md) | Utilisé pour suivre les énumérations dans lesquelles plusieurs appels de fonction sont requis. |
| [**\_handle LSA**](lsa-handle.md)                          | Handle vers un objet de [**stratégie**](policy-object.md) .                       |



 

 

 
