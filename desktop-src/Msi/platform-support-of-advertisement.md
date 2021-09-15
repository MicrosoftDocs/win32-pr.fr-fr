---
description: le Windows Installer prend en charge la publication d’applications et de fonctionnalités.
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: Prise en charge des plateformes de la publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413964"
---
# <a name="platform-support-of-advertisement"></a>Prise en charge des plateformes de la publication

le Windows Installer prend en charge la publication d’applications et de fonctionnalités.

les fonctionnalités de publication suivantes sont disponibles sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003, Windows XP et Windows 2000.

-   Raccourcis et leurs icônes.

-   Extensions et leurs icônes spécifiées dans la [table ProgID](progid-table.md).

-   Verbes de Shell et de commande inscrits sous la clé ProgId.

-   Contextes CLSID et InProcHandler.

-   l’installation à la demande via OLE est disponible uniquement par programmation via [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++) et la **fonction CreateObject (Visual Basic)** ou la **fonction GetObject (Visual Basic)**.

> [!Note]
> Les informations AppId et TypeLib sont écrites uniquement lorsqu’un composant publié est installé.
> 
> Pour prendre en charge les extensions de nom de fichier, l’application doit être publiée sur Active Directory par un administrateur à l’aide de stratégie de groupe.

## <a name="remarks"></a>Notes

L’installation du produit peut ne pas nécessiter un redémarrage, mais tous les raccourcis publiés ne fonctionnent pas tant que l’ordinateur n’est pas redémarré. Les raccourcis publiés des installations suivantes fonctionnent sans redémarrage.

Pour garantir le bon fonctionnement des raccourcis publiés, l’auteur du package doit planifier un redémarrage forcé à la fin de l’installation.

pour éviter les redémarrages inutiles du système, planifiez un redémarrage pour qu’il s’exécute uniquement si aucune version du Windows Installer n’est installée.

Les instructions conditionnelles peuvent vérifier la propriété [**ShellAdvtSupport**](shelladvtsupport.md) et la propriété [**Version9X**](version9x.md) . Pour plus d’informations sur la planification d’un redémarrage forcé conditionnel, consultez [redémarrages système](system-reboots.md) et [utilisation de propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).

 

 
