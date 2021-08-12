---
title: Traitement des domaines et manipulation des attributs
description: Le traitement des domaines, également appelé manipulation des attributs, fait référence à la transformation du nom de l’utilisateur qui demande l’accès.
ms.assetid: 52963eda-ea95-4307-8924-d4143bc1f53d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8054ad8234ca4772a52619d83bc85a9d357f2cf8da2f1c969eed918c75a8305a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618945"
---
# <a name="realms-processing-and-attribute-manipulation"></a>Traitement des domaines et manipulation des attributs

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

Le traitement des domaines, également appelé manipulation des attributs, fait référence à la transformation du nom de l’utilisateur qui demande l’accès. L’ID de station d’appel et l’ID de station appelée peuvent également être manipulés. Les règles de traitement des domaines font partie de la collection d’attributs de profil proxy.

Pour chaque manipulation, vous devez créer deux attributs de [règle de manipulation](/windows/desktop/Nps/sdo-manipulation-rule) . Chacun de ces attributs est une valeur de chaîne. La première règle contient une expression régulière représentant le modèle à faire correspondre. La deuxième règle contient une expression régulière qui représente le texte de remplacement. Vous devez également créer un attribut [manipulation-Target](/windows/desktop/Nps/sdo-manipulation-target) . Cet attribut est une énumération qui spécifie quelle partie des informations de l’utilisateur doit être manipulée.

L’ordre dans lequel les attributs sont créés est important. NPS traite les attributs dans l’ordre dans lequel ils ont été créés.

Le tableau suivant montre un exemple d’un ensemble d’attributs de manipulation.



| Nom                 | Type         | Valeur de chaîne     |
|----------------------|--------------|------------------|
| msManipulationRule   | **VT \_ BSTR** | "@company.com"   |
| msManipulationRule   | **VT \_ BSTR** | "@microsoft.com" |
| msManipulationRule   | **VT \_ BSTR** | "^.+@"           |
| msManipulationRule   | **VT \_ BSTR** | « guest@ »         |
| msManipulationTarget | **VT \_**   | "1"              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hiérarchie du modèle objet](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[Attributs pris en charge par SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> <dt>

[Création d’une stratégie de demande de connexion](/windows/desktop/Nps/sdo-creating-a-connection-request-policy)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[**ISdoDictionaryOld**](/windows/desktop/api/sdoias/nn-sdoias-isdodictionaryold)
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 