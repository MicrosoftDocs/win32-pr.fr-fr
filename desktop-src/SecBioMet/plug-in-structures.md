---
title: Structures de plug-in
description: Structures pour le développement d’applications clientes par l’API Windows Biometric Framework.
ms.assetid: 64fb908c-72c2-4639-a2f6-77ede080512c
keywords:
- Windows api de l’infrastructure biométrique Windows Biometric Framework, structures de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e150dd043a8c95e91d0f9095e23584544f43a503a709ae54c9180e06aa40bdaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101239"
---
# <a name="plug-in-structures"></a>Structures de plug-in

les structures suivantes sont prises en charge pour le développement d’applications clientes par l’API Windows Biometric Framework.

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

 

 





