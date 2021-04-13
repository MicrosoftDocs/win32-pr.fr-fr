---
title: Structures de plug-in
description: Structures pour le développement d’applications clientes par l’API Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- API Windows Biometric Framework API Windows Biometric Framework, structures de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193b5a99f30c76e8e6e2ab7ebf0242cf56905816
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310877"
---
# <a name="plug-in-structures"></a>Structures de plug-in

Les structures suivantes sont prises en charge pour le développement d’applications clientes par l’API Windows Biometric Framework.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                | Description                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_stratégie de compte WINBIO \_**](winbio-account-policy.md)<br/>                                  | Contient une stratégie d’antiusurpation propre à la valeur par défaut ou spécifique au compte.<br/>                                                         |
| [**VERSION de l’interface de l' \_ adaptateur WINBIO \_ \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_adapter_interface_version)<br/>           | Contient un numéro de version majeure et mineure utilisé dans les tables du moteur, du capteur et de l’interface de l’adaptateur de stockage.<br/>                |
| [**\_interface du moteur WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface)<br/>                              | Contient des pointeurs vers vos fonctions d’adaptateur de moteur personnalisées.<br/>                                                                 |
| [**\_paramètres d' \_ inscription étendue WINBIO \_**](winbio-extended-enrollment-parameters.md)<br/> | Contient des informations supplémentaires nécessaires à un adaptateur de moteur pour créer un modèle d’inscription. <br/>                            |
| [**\_pipeline WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_pipeline)<br/>                                               | Contient les informations de contexte partagé utilisées par les composants de capteur, de moteur et d’adaptateur de stockage dans une seule unité biométrique.<br/> |
| [**\_interface du capteur WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface)<br/>                              | Contient des pointeurs vers vos fonctions d’adaptateur de capteur personnalisées.<br/>                                                                 |
| [**\_interface de stockage WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface)<br/>                            | Contient des pointeurs vers vos fonctions d’adaptateur de stockage personnalisées.<br/>                                                                |
| [**\_enregistrement de stockage WINBIO \_**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_record)<br/>                                  | Contient un modèle biométrique et les données associées dans un format standard.<br/>                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du plug-in](plug-in-reference.md)
</dt> <dt>

[Fonctions de plug-in](plug-in-functions.md)
</dt> <dt>

[**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)
</dt> <dt>

[**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)
</dt> <dt>

[**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)
</dt> </dl>

 

 





