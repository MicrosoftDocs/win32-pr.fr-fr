---
description: VDS fournit des objets pour effectuer des activités liées aux services. Cette rubrique décrit chaque objet.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Objets de démarrage et de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60a87c7e52a263d03e80f44911f72db5f49259baf33a7b2f90680f30bb3b2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125929"
---
# <a name="startup-and-service-objects"></a>Objets de démarrage et de service

\[à partir de Windows 8 et Windows Server 2012, l’interface COM du [Service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion des Stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS fournit des objets pour effectuer des activités liées aux services. Cette rubrique décrit chaque objet.

## <a name="service-loader-object"></a>Objet de chargeur de service

L’objet chargeur de service fournit les méthodes utilisées par les applications pour charger et initialiser VDS. Pour préparer le VDS en vue de son utilisation, une application doit effectuer les opérations suivantes :

-   Créez une instance de l’objet chargeur de service, qui retourne l’interface [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) .
-   Appelez la méthode [**IVdsServiceLoader :: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) pour charger le service.

Pour obtenir un exemple de code, consultez [chargement de VDS](loading-vds.md).

Autorisez toujours l’initialisation complète du service avant d’appeler les méthodes exposées par l’objet de service. Utilisez la méthode [**IVdsService :: IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) pour déterminer l’état du processus de chargement. Utilisez la méthode [**IVdsService :: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) pour bloquer les appels aux objets VDS jusqu’à ce que l’initialisation se termine.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.

| Type                                              | Élément                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Énumérations associées                           | Aucun.                                           |
| Structures associées                             | Aucun.                                           |



 

## <a name="service-object"></a>Objet de service

L’objet de service est un objet multifonctionnel qui est central pour toutes les applications VDS. Avec cet objet, un appelant peut effectuer les opérations suivantes :

-   Déterminez l’état de l’initialisation du service.
-   Récupérez tous les fournisseurs de matériel ou de logiciels inscrits auprès de VDS.
-   Rapport sur les disques non alloués.
-   Retourne le type de système de fichiers et la lettre de lecteur associés aux volumes sur un disque.
-   Supprimez les chemins d’accès en mode utilisateur inutilisés et les dossiers montés du Registre, puis actualisez les disques.
-   Recevoir des notifications VDS.
-   Redémarrez l’hôte.
-   Récupérez Fibre Channel ports HBA ou des adaptateurs d’initiateur iSCSI sur l’ordinateur local.
-   Préparez en toute sécurité les numéros d’unités logiques exposés en tant que disques sur l’ordinateur local en vue de leur suppression.

Les structures de notification VDS transmettent les GUID d’objet à toutes les applications qui sont inscrites auprès de VDS pour recevoir des notifications. Utilisez la méthode [**IVdsService :: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) pour convertir un GUID d’objet en un pointeur d’objet. Pour obtenir une description plus complète du modèle de notification, consultez la page [notifications VDS](vds-notification-model.md).

Le tableau suivant répertorie les interfaces, énumérations et structures associées. 

| Type                                                                   | Élément                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfaces qui sont toujours implémentées mais ne sont pas exposées aux applications | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Énumérations associées                                                | [**VDS \_ \_ \_ indicateur de fournisseur de requêtes**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**\_ \_ type d’objet VDS**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**\_ \_ indicateur de service VDS**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), indicateur de [**\_ \_ lettre \_ de lecteur VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), indicateur de [**\_ \_ système \_ de fichiers VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), [**\_ \_ \_ \_ indicateur de prop de système de fichiers VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Structures associées                                                  | [**VDS \_ SERVICE \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**système de fichiers VDS \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), [**type de système de fichiers VDS \_ \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), message de [**\_ lettre de lecteur \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), notification du [**\_ système de fichiers \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**notification de \_ point de montage \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows server 2003 :** ces interfaces ne sont pas prises en charge tant que Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Objet adaptateur de l’initiateur

Un objet adaptateur d’initiateur modélise un adaptateur d’initiateur iSCSI sur l’ordinateur hôte du service VDS. Le service VDS peut uniquement afficher les adaptateurs initiateur sur l’ordinateur local. Le rôle d’un objet adaptateur de l’initiateur est de gérer les sessions de connexion entre l’ordinateur local et les cibles iSCSI.

Le tableau suivant répertorie les interfaces, énumérations et structures associées. 

| Type                                              | Élément                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Énumérations associées                           | [**VDS \_ \_ \_ type de connexion iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ \_ \_ indicateur de connexion iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**\_ \_ \_ type d’authentification iSCSI VDS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Structures associées                             | [**VDS \_ carte de l' \_ initiateur iSCSI \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows server 2003 :** cette interface n’est pas prise en charge tant que Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Objet portail de l’initiateur

Un objet portail de l’initiateur modélise un portail initiateur iSCSI sur un initiateur iSCSI. Un portail initiateur est la combinaison d’une adresse IP et d’un port par le biais duquel un ordinateur hôte se connecte à un portail sur un sous-système iSCSI. Le rôle d’un objet portail de l’initiateur est de servir de l’un des points de terminaison d’un chemin d’accès MPIO et de configurer les paramètres de sécurité IPSEC.

Le tableau suivant répertorie les interfaces, énumérations et structures associées. 

| Type                                              | Élément                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Énumérations associées                           | [**VDS \_ \_ \_ indicateur IPSec iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Structures associées                             | [**VDS \_ portail de l' \_ initiateur iSCSI \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**\_ \_ \_ clé IPSec iSCSI VDS**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**\_ adresse IP VDS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows server 2003 :** cette interface n’est pas prise en charge tant que Windows Server 2003 R2.

## <a name="hba-port-object"></a>Objet port HBA

L’objet port HBA modélise une Fibre Channel Port d’adaptateur de bus hôte (HBA).

Utilisez la méthode [**IVdsServiceHba :: QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) pour déterminer les ports HBA connus du VDS sur l’ordinateur local.

Le tableau suivant répertorie les interfaces, énumérations et structures associées.

| Type                                              | Élément                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces toujours exposées par cet objet | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Énumérations associées                           | [**VDS \_ HBAPORT \_ type**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**\_ \_ État de VDS HBAPORT**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**\_ indicateur de \_ Vitesse \_ VDS HBAPORT**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Structures associées                             | [**VDS \_ HBAPORT \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows server 2003 :** cette interface n’est pas prise en charge tant que Windows Server 2003 R2.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Chargement de VDS](loading-vds.md)
</dt> <dt>

[**IVdsService :: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notifications VDS](vds-notification-model.md)
</dt> </dl>

 

 
