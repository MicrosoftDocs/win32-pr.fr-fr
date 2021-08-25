---
description: Un descripteur de sécurité contient les informations de sécurité associées à un objet sécurisable.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Descripteurs de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1049becf755bbb0940cfd5def3b59662a20eb2a690d90a36e06c5706212f02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907189"
---
# <a name="security-descriptors"></a>Descripteurs de sécurité

Un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) contient les informations de sécurité associées à un [objet sécurisable](securable-objects.md). Un descripteur de sécurité se compose d’une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) et des informations de sécurité qui lui sont associées. Un descripteur de sécurité peut inclure les informations de sécurité suivantes :

-   [Identificateurs de sécurité](security-identifiers.md) (SID) pour le propriétaire et le groupe principal d’un objet.
-   [Liste DACL](access-control-lists.md) qui spécifie les droits d’accès accordés ou refusés à des utilisateurs ou des groupes particuliers.
-   [SACL](access-control-lists.md) qui spécifie les types de tentatives d’accès qui génèrent des enregistrements d’audit pour l’objet.
-   Ensemble de bits de contrôle qui qualifient la signification d’un descripteur de sécurité ou de ses membres individuels.

Les applications ne doivent pas manipuler directement le contenu d’un descripteur de sécurité. l’API Windows fournit des fonctions permettant de définir et de récupérer les informations de sécurité dans le descripteur de sécurité d’un objet. En outre, il existe des fonctions permettant de créer et d’initialiser un descripteur de sécurité pour un nouvel objet.

les Applications qui utilisent des descripteurs de sécurité sur des objets Active Directory peuvent utiliser les fonctions de sécurité Windows ou les interfaces de sécurité fournies par les interfaces de Service Active Directory (ADSI). Pour plus d’informations sur les interfaces de sécurité ADSI, consultez fonctionnement [de Access Control dans Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).

 

 
