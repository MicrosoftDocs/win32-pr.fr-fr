---
description: Une liste de contrôle d’accès aux objets peut contenir des ACE qu’elle a héritées de son conteneur parent.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Héritage ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013738"
---
# <a name="ace-inheritance"></a>Héritage ACE

La liste de contrôle d’accès d’un objet peut contenir des ACE qu’il a hérité de son conteneur parent. Par exemple, une sous-clé de Registre peut hériter des ACE de la clé située au-dessus de celle-ci dans la hiérarchie du Registre. De même, un fichier dans un système de fichiers NTFS peut hériter des ACE du répertoire qui le contient.

La structure d' [**\_ en-tête ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) d’une entrée du contrôle d’accès contient un jeu d’indicateurs d’héritage qui contrôlent l’héritage ACE et l’effet d’une entrée du contrôle d’accès sur l’objet auquel elle est attachée. Le système interprète les indicateurs d’héritage et d’autres informations d’héritage en fonction [des règles d’héritage de l’entrée du contrôle d'](ace-inheritance-rules.md)accès.

Ces règles ont été améliorées avec les fonctionnalités suivantes :

-   Prise en charge de la [propagation automatique des ACE pouvant être héritées](automatic-propagation-of-inheritable-aces.md).
-   Indicateur qui fait la distinction entre les ACE héritées et les ACE qui ont été directement appliquées à un objet.
-   Entrées de contrôle d’accès spécifiques aux objets qui vous permettent de spécifier le type d’objet enfant qui peut hériter de l’entrée du contrôle d’accès.
-   la possibilité d’empêcher une liste dacl ou SACL d’hériter des entrées du contrôle d’accès en définissant la SE \_ liste de \_ contrôle d’accès discrétionnaire protégée ou SE \_ \_ bits protégés par la liste de contrôle d’accès dans les bits de contrôle [*du descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) , à l’exception de l’ace et de l' \_ \_ \_ \_ \_ ID de stratégie système \_ \_

 

 
