---
description: Lorsque vous créez un objet sécurisable, vous pouvez assigner un descripteur de sécurité au nouvel objet.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descripteurs de sécurité pour les nouveaux objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3f9af674c83e4fc42448635bc54dfc0bb51b42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514221"
---
# <a name="security-descriptors-for-new-objects"></a>Descripteurs de sécurité pour les nouveaux objets

Lorsque vous créez un objet sécurisable, vous pouvez assigner un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) au nouvel objet. Les fonctions permettant de créer des objets sécurisables, tels que [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), ont un paramètre qui pointe vers la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) qui peut contenir un pointeur vers le descripteur de sécurité du nouvel objet. Pour obtenir un exemple de code qui génère un descripteur de sécurité, puis appelle **RegCreateKeyEx** pour affecter le descripteur de sécurité à une nouvelle clé de Registre, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).

Le composant système ou le serveur qui gère l’objet peut stocker le descripteur de sécurité spécifié ou par défaut pour en faire un attribut persistant de l’objet. Si le créateur d’un objet ne spécifie pas de descripteur de sécurité, le système utilise les informations de sécurité héritées ou par défaut pour créer un descripteur de sécurité. Vous pouvez utiliser des fonctions pour modifier les informations dans le descripteur de sécurité d’un objet.

Les objets de service d’annuaire, les fichiers, les répertoires, les clés de Registre et les ordinateurs de bureau sont des objets sécurisables qui peuvent avoir un objet parent. Lorsque vous créez l’un de ces objets, le système recherche les ACE pouvant être héritées dans le descripteur de sécurité de l’objet parent. Le système fusionne généralement les ACE pouvant être héritées dans les listes de contrôle d’accès du descripteur de sécurité du nouvel objet. Vous pouvez empêcher une liste DACL ou SACL d’hériter des entrées du contrôle d’accès en définissant les \_ \_ bits de contrôle du descripteur DACL protected ou se se trouvent \_ \_ dans les bits de contrôle du descripteur de sécurité. Pour plus d’informations, consultez [héritage de l’entrée](ace-inheritance.md)du contrôle d’accès.

 

 
