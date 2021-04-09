---
title: Read-Only les contrôleurs de schéma et le schéma de Active Directory
description: Windows Server 2008 introduit un nouveau type de contrôleur de domaine, le contrôleur de domaine en lecture seule (RODC).
ms.assetid: 9d9082d2-6f7f-4ffa-b8c7-6414be764d0c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4284ffdda7ed2fbe481c201f7da69371209ce55
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102496"
---
# <a name="read-only-dcs-and-the-active-directory-schema"></a>Read-Only les contrôleurs de schéma et le schéma de Active Directory

Windows Server 2008 introduit un nouveau type de contrôleur de domaine, le contrôleur de domaine en lecture seule (RODC). Cela fournit un contrôleur de domaine à utiliser dans les succursales où un contrôleur de domaine complet ne peut pas être placé. L’objectif est de permettre aux utilisateurs des succursales de se connecter et d’effectuer des tâches telles que le partage de fichiers et d’imprimantes, même en l’absence de connectivité réseau avec les sites hub.

RODC ne change pas la manière dont le schéma est utilisé. Toutefois, il est utile de mentionner que le schéma prend en charge une Read-Only ensemble d’attributs partiels (Roll-pas), également appelé jeu d’attributs filtré RODC, qui est un ensemble d’attributs spéciaux qui n’est pas répliqué sur RODC pour des raisons de sécurité. RO-pas sont définis dans le schéma via l’attribut [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) .

## <a name="rodc-filtered-attribute-set"></a>Jeu d’attributs filtré RODC

Certaines applications qui utilisent [Active Directory Domain Services](active-directory-domain-services.md) en tant que magasin de données peuvent avoir des données de type informations d’identification (telles que des mots de passe, des informations d’identification ou des clés de chiffrement) qui ne doivent pas être stockées sur un contrôleur de domaine Read-Only au cas où le RODC serait volé ou compromis. Pour ce type d’application, vous pouvez ajouter l’attribut à l’ensemble d’attributs filtré de RODC pour l’empêcher de se répliquer sur RODC dans la forêt, et marquer l’attribut comme confidentiel, ce qui supprime la capacité à lire les données pour les membres du groupe utilisateurs authentifiés (y compris les contrôleurs de domaine en lecture seule).

## <a name="adding-attributes-to-the-rodc-filtered-attribute-set"></a>Ajout d’attributs à l’ensemble d’attributs filtré RODC

L’ensemble d’attributs filtrés RODC est un ensemble dynamique d’attributs qui n’est pas répliqué sur un RODC de la forêt. Vous pouvez configurer l’ensemble d’attributs filtrés RODC sur un contrôleur de schéma qui exécute Windows Server 2008. Lorsque les attributs ne peuvent pas être répliqués sur RODC, ces données ne peuvent pas être exposées inutilement si un RODC est volé ou compromis.

Vous ne pouvez pas ajouter d’attributs système critiques à l’ensemble d’attributs filtré RODC. Un attribut est essentiel du système s’il est requis pour AD DS, l’autorité de sécurité locale (LSA), le gestionnaire de comptes de sécurité (SAM) et l’un des fournisseurs de services de sécurité spécifiques à Microsoft, tels que le protocole d’authentification Kerberos, pour fonctionner correctement. Dans les versions de Windows Server 2008 après la version bêta 3, un attribut critique du système a une valeur d’attribut schemaFlagsEx égale à (valeur d’attribut schemaFlagsEx & 0x1 = **true**).

Pour obtenir des instructions pas à pas sur l’ajout d’attributs à l’ensemble d’attributs filtré RODC, consultez [l’annexe D du Guide pas à pas pour]( /previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc772331(v=ws.10))les contrôleurs de domaine en lecture seule.

## <a name="marking-attributes-as-confidential"></a>Marquage des attributs comme confidentiels

En outre, il est recommandé de marquer également comme confidentielles tous les attributs que vous configurez dans le cadre de l’ensemble d’attributs filtré RODC. Pour marquer un attribut comme confidentiel, vous devez supprimer l’autorisation de lecture pour l’attribut du groupe utilisateurs authentifiés. Le marquage de l’attribut comme confidentiel offre une protection supplémentaire contre un RODC compromis en supprimant les autorisations nécessaires pour lire les données de type informations d’identification. Pour plus d’informations sur le marquage des attributs comme confidentiels, voir [l’article 922836 de la base de connaissances Microsoft]( https://support.microsoft.com/kb/922836).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide pas à pas pour les contrôleurs de domaine en lecture seule]( https://support.microsoft.com/kb/922836)
</dt> </dl>

 

 