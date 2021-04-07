---
description: Vous pouvez écrire des modules de stratégie dans le langage de programmation C, C++ ou Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Écriture de modules personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952113"
---
# <a name="writing-custom-modules"></a>Écriture de modules personnalisés

Vous pouvez écrire des modules de stratégie dans le langage de programmation C, C++ ou Visual Basic. Le compilateur Microsoft requis est disponible dans Visual C++ version 5,0 ou ultérieure, ou dans Visual Basic version 5,0 ou ultérieure. Une [*autorité de certification*](../secgloss/c-gly.md) d’entreprise (ca) doit utiliser uniquement le module de stratégie d’entreprise fourni par Microsoft.

Vous devez implémenter [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) lors de l’écriture d’un module de stratégie personnalisé. En outre, vous devez implémenter [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) lors de l’écriture d’un module de stratégie personnalisé.

Les modules de stratégie peuvent appeler des méthodes à partir de [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) pour faciliter le traitement d’une [*demande de certificat*](../secgloss/c-gly.md); **ICertServerPolicy** permet de définir et d’extraire des propriétés et des extensions de certificat.

Pour plus d'informations, consultez les rubriques ci-dessous.



| Rubrique                                                                      | Description                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [Définition des propriétés d’un certificat](setting-certificate-properties.md)       | Définition des propriétés d’un certificat |
| [Écriture de modules de sortie personnalisés](writing-custom-exit-modules.md)             | Écriture de modules de sortie personnalisés             |
| [Écriture de gestionnaires d’extensions personnalisés](writing-custom-extension-handlers.md) | Écriture de gestionnaires d’extensions personnalisés       |



 

 

 
