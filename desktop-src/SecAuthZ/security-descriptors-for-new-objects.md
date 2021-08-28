---
description: Lorsque vous créez un objet sécurisable, vous pouvez assigner un descripteur de sécurité au nouvel objet.
ms.assetid: 5b276d27-31a4-4a83-83b0-c4044a427097
title: Descripteurs de sécurité pour les nouveaux objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38edc927f1f017e3f102194b0a4aac5d0442ec730e8480a00c054add0935a62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907339"
---
# <a name="security-descriptors-for-new-objects"></a>Descripteurs de sécurité pour les nouveaux objets

Lorsque vous créez un objet sécurisable, vous pouvez assigner un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) au nouvel objet. Les fonctions permettant de créer des objets sécurisables, tels que [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa), ont un paramètre qui pointe vers la structure des [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) qui peut contenir un pointeur vers le descripteur de sécurité du nouvel objet. Pour obtenir un exemple de code qui génère un descripteur de sécurité, puis appelle **RegCreateKeyEx** pour affecter le descripteur de sécurité à une nouvelle clé de Registre, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md).

Le composant système ou le serveur qui gère l’objet peut stocker le descripteur de sécurité spécifié ou par défaut pour en faire un attribut persistant de l’objet. Si le créateur d’un objet ne spécifie pas de descripteur de sécurité, le système utilise les informations de sécurité héritées ou par défaut pour créer un descripteur de sécurité. Vous pouvez utiliser des fonctions pour modifier les informations dans le descripteur de sécurité d’un objet.

Les objets de service d’annuaire, les fichiers, les répertoires, les clés de Registre et les ordinateurs de bureau sont des objets sécurisables qui peuvent avoir un objet parent. Lorsque vous créez l’un de ces objets, le système recherche les ACE pouvant être héritées dans le descripteur de sécurité de l’objet parent. Le système fusionne généralement les ACE pouvant être héritées dans les listes de contrôle d’accès du descripteur de sécurité du nouvel objet. vous pouvez empêcher une liste dacl ou SACL d’hériter des entrées du contrôle d’accès en définissant la SE \_ liste de \_ contrôle d’accès discrétionnaire protégée ou SE \_ \_ bits protégés dans les bits de contrôle du descripteur de sécurité. Pour plus d’informations, consultez [héritage de l’entrée](ace-inheritance.md)du contrôle d’accès.

 

 
