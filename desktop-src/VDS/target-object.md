---
description: Objet cible
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: Objet cible
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1e81ea94a2f608378eba069defc83a721e0fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521971"
---
# <a name="target-object"></a>Objet cible

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objet cible modélise une cible iSCSI contenue dans un sous-système iSCSI.

Utilisez la méthode [**IVdsSubSystemIscsi :: QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) pour déterminer les cibles iSCSI du sous-système. Les appelants peuvent obtenir un pointeur vers une cible spécifique en sélectionnant l’objet cible souhaité à partir de l’énumération retournée par la méthode **QueryTargets** . Avec un objet cible, vous pouvez définir le nom convivial et la requête de la cible pour les propriétés cibles, les numéros d’unités logiques associés et le sous-système qui contient la cible.

Les ordinateurs hôtes doivent se connecter aux cibles pour accéder aux numéros d’unités logiques qui leur sont associés. Pour effectuer une ouverture de session sur une cible, la cible doit avoir au moins un portail associé dans l’un de ses groupes de portails. L’entrée et la sortie des numéros d’unités logiques associés sont gérées par le biais de cette session de connexion.

Les propriétés de l’objet cible incluent un identificateur d’objet, un nom iSCSI, un nom convivial et un indicateur CHAP.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.



| Type                                                                                      | Élément                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet dans les fournisseurs iSCSI VDS 1,1 et 2,0 uniquement | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget).                                                                                 |
| Énumérations associées                                                                   | Aucun                                                                                                                       |
| Structures associées                                                                     | [**VDS \_ La \_ \_ prop cible iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) et la [**\_ \_ notification cible VDS**](/windows/desktop/api/Vds/ns-vds-vds_target_notification). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets de fournisseur de matériel](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
