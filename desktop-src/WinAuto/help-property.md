---
title: Help, propriété
description: La propriété Help fournit des informations qui indiquent à l’utilisateur la fonction d’un objet.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309902"
---
# <a name="help-property"></a>Help, propriété

La propriété **Help** fournit des informations qui indiquent à l’utilisateur la fonction d’un objet.

La propriété **Help** est récupérée en appelant [**IAccessible :: obtenir \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Cette propriété contient des informations de style Balloon (telles qu’elles figurent dans les info-bulles) utilisées pour décrire ce que fait l’objet ou comment l’utiliser. Par exemple, la propriété d' **aide** d’un bouton de barre d’outils qui affiche une imprimante peut fournir le texte suivant : « imprime le document actif ».

Le texte de la propriété **d’aide** n’a pas besoin d’être unique au sein de l’interface utilisateur.

## <a name="when-to-support-the-help-property"></a>Quand prendre en charge la propriété d’aide

Les serveurs ne prennent pas en charge la propriété **d’aide** si d’autres propriétés fournissent des informations suffisantes sur le rôle de l’objet et les actions effectuées par l’objet. Les objets accessibles qui exposent des contrôles fournis par le système ne prennent pas en charge la propriété **Help** .

 

 




