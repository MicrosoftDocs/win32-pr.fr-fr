---
description: Les fonctions et les structures de contexte d’activation sont utilisées avec les assemblys côte à côte.
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: Référence du contexte d’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d6f8225b4db8b22227edf2b779ed9e1b50da7a3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238163"
---
# <a name="activation-context-reference"></a>Référence du contexte d’activation

Les fonctions et les structures de contexte d’activation sont utilisées avec les assemblys côte à côte.

Le tableau suivant répertorie les fonctions de contexte d’activation.



| Fonction                                                   | Description                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | Active le contexte d’activation spécifié.                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | Incrémente le décompte de références du contexte d’activation spécifié.                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | Crée un contexte d’activation.                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | Désactive le contexte d’activation spécifié.                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | Retourne les données contenues dans la structure de [**\_ \_ \_ données de la section ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) qui correspond au GUID spécifié.   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | Retourne les données contenues dans la structure de [**\_ \_ \_ données de la section ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) qui correspond à la chaîne spécifiée. |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | Retourne le contexte d’activation actuel.                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | Garantit que la mémoire est libérée lorsqu’un manifeste est chargé, déchargé et rechargé.                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | Interroge le contexte d’activation pour obtenir des informations sur un assembly ou un fichier.                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | Spécifie l’espace de noms et le nom d’attribut de l’attribut à interroger.                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | Décrémente le décompte de références du contexte d’activation spécifié.                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | Désactive le contexte d’activation spécifié, mais ne le libère pas.                                                                               |



 

Le tableau suivant répertorie les structures de contexte d’activation.



| Structure                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ informations détaillées sur l’assembly du contexte d’activation \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | Contient des informations détaillées sur le contexte d’activation.                                                                                                                                                                                                                                                                                                                                  |
| [**\_ \_ informations détaillées du contexte d’activation \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | Contient des informations sur l’assembly dans le contexte d’activation.                                                                                                                                                                                                                                                                                                                           |
| [**\_index de \_ requête du contexte d’activation \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | Contient l’assembly dans le contexte d’activation et l’index du fichier au sein de l’assembly.                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | Contient des informations qui décrivent un contexte d’activation spécifique.                                                                                                                                                                                                                                                                                                                           |
| [**données de la \_ section ACTCTX \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | Retourne les informations de contexte d’activation avec le GUID ou la section de contexte d’activation avec balises d’entier 32 bits.                                                                                                                                                                                                                                                                   |
| [**\_ \_ informations détaillées sur le fichier \_ d’assembly**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | Contient des informations sur un fichier de l’assembly dans le contexte d’activation.                                                                                                                                                                                                                                                                                                                 |
| [**\_ \_ \_ informations sur le niveau d’exécution du contexte d’activation \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | Utilisé par la fonction [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2003 et Windows XP :** Cette structure n’est pas disponible.<br/>                                                                                                                                                                                                                                    |
| [**\_élément de contexte de compatibilité \_**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | Utilisé par la fonction [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) dans le cadre de la structure des informations de compatibilité du contexte d' [**Activation \_ \_ \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) . <br/> **Windows Server 2008 et versions antérieures, et Windows Vista et versions antérieures :** Cette structure n’est pas disponible. il est disponible à partir de Windows Server 2008 R2 et Windows 7.<br/> |
| [**\_informations de \_ compatibilité du contexte d’activation \_**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | Utilisé par la fonction [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) .<br/> **Windows Server 2008 et versions antérieures, et Windows Vista et versions antérieures :** Cette structure n’est pas disponible. il est disponible à partir de Windows Server 2008 R2 et Windows 7.<br/>                                                                                                                                   |



 

Le tableau suivant répertorie les énumérations de contexte d’activation.

| Énumération                                                                       | Description                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_niveau d' \_ exécution \_ demandé par ACTCTX**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | Décrit le niveau d’exécution demandé du contexte d’activation. **Windows Server 2003 et Windows XP :** Cette énumération n’est pas disponible.<br/>                                                                                                      |
| [**\_type d' \_ élément de compatibilité ACTCTX \_**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | Décrit l’élément Compatibility dans le manifeste de l’application. **Windows Server 2008 et versions antérieures, et Windows Vista et versions antérieures :** Cette énumération n’est pas disponible. il est disponible à partir de Windows Server 2008 R2 et Windows 7.<br/> |



 

 

