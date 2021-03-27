---
description: Cette rubrique fournit des informations sur les considérations relatives à la sécurité de GDI. Cette rubrique ne fournit pas tout ce dont vous avez besoin pour connaître les problèmes de sécurité. Au lieu de cela, utilisez-le comme point de départ et référence pour ce domaine technologique.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considérations relatives à la sécurité : GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952443"
---
# <a name="security-considerations-gdi"></a>Considérations relatives à la sécurité : GDI

Cette rubrique fournit des informations sur les considérations relatives à la sécurité de GDI. Cette rubrique ne fournit pas tout ce dont vous avez besoin pour connaître les problèmes de sécurité. Au lieu de cela, utilisez-le comme point de départ et référence pour ce domaine technologique.

GDI rencontre généralement des problèmes de sécurité, car il gère l’affichage plutôt que l’entrée. Toutefois, voici quelques-uns des problèmes que vous devez prendre en compte.

Les bitmaps, les sous-fichiers et les polices sont des structures complexes qui pourraient être endommagées. Il est conseillé d’essayer de s’assurer que ces éléments ne sont pas endommagés et qu’ils proviennent d’une source digne de confiance.

Une application peut spécifier le descripteur de sécurité pour certaines des API d’impression et de mise en file d’attente. Vous devez veiller à définir le descripteur de sécurité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Centre de sécurité Microsoft](https://www.microsoft.com/security/)
</dt> <dt>

[Centre de développement Sécurité](https://technet.microsoft.com/security/)
</dt> <dt>

[Centre de Sécurité TechNet](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



