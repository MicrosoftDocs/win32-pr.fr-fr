---
description: le fournisseur Windows Driver Model (WDM) accorde l’accès aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au modèle WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Accès aux données à partir des pilotes de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bec478f83ddbc6d58419710fb868ddd233f820a06004210c1dac495de86b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131912"
---
# <a name="accessing-data-from-device-drivers"></a>Accès aux données à partir des pilotes de périphérique

le fournisseur Windows Driver Model (WDM) accorde l’accès aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au modèle WDM. Les classes pour les pilotes de matériel résident dans l' \\ \\ \\ espace de noms WMI racine.

Le fournisseur WDM présente un intérêt pour ceux qui écrivent des pilotes de périphérique et pour les administrateurs qui sont intéressés par les données de pilote de périphérique.

Les sections suivantes sont présentées dans cette rubrique :

-   [Informations pour les writers de pilote de périphérique](#information-for-device-driver-writers)
-   [Informations pour les administrateurs et les utilisateurs des données de pilote](#information-for-administrators-and-users-of-driver-data)
-   [Rubriques connexes](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informations pour les writers de pilote de périphérique

Les classes WMI associées à un pilote de périphérique spécifique sont créées lorsque le fournisseur WDM extrait le fichier MOF binaire à partir du fichier exécutable du pilote de périphérique. Cette opération a lieu chaque fois que WMI est démarré, qu’un nouveau pilote de périphérique est installé ou que l’instance de [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) pour un pilote particulier est supprimée. En consultant wmiprov. log, vous pouvez déterminer si une erreur provoquant un échec s’est produite lors de l’extraction du fichier MOF binaire. Les détails des erreurs [mofcomp](mofcomp.md) sont signalés dans mofcomp. log. Pour plus d’informations, consultez [fichiers journaux WMI](wmi-log-files.md). Pour des raisons de performances, le fournisseur WDM ne génère pas d’événements lors de la création ou de la suppression de classes en raison du démarrage ou de l’arrêt d’un fournisseur WDM.

Le fournisseur WDM transforme toutes les données WNODE en informations de classe. Si une erreur se produit lors de la transformation des données de WNODE en données de classe, elles sont signalées dans wmiprov. log avec l’en-tête formaté et les octets rendus sous la même forme qu’une image mémoire.

Les modifications apportées aux paramètres de sécurité des pilotes ne prennent effet qu’une fois le fournisseur WDM déchargé et rechargé. Pour plus d’informations, consultez [déchargement d’un fournisseur](unloading-a-provider.md).

WMI peut également rendre disponibles des compteurs de performances élevées pour les pilotes matériels. Pour plus d’informations sur la création de classes à hautes performances et l’affichage des données dans le moniteur système PerfMon, consultez [amélioration de l’efficacité d’un fournisseur d’instances](improving-the-efficiency-of-an-instance-provider.md). Pour plus d’informations sur l’écriture de pilotes de périphérique compatibles WMI, consultez [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Pour plus d’informations sur les qualificateurs spécifiques à WDM dans le fichier MOF, consultez [**qualificateurs spécifiques au fournisseur WDM**](qualifiers-specific-to-the-wdm-provider.md).

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informations pour les administrateurs et les utilisateurs des données de pilote

Le fait de répertorier les instances de la classe [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) fournit une liste des pilotes du système et des informations indiquant si le fournisseur WDM a réussi à compiler les MOF pour chaque pilote. Vous pouvez forcer le fournisseur à recompiler et à régénérer les classes d’un pilote en supprimant l’instance de WMIBinaryMofResource qui représente ce pilote. Les détails des erreurs [mofcomp](mofcomp.md) sont signalés dans le fichier mofcomp. log.

Si l’espace de noms WMI est endommagé, il peut être supprimé et rouvert pour forcer le WDM à reconstruire les classes du pilote. Pour plus d’informations sur l’ouverture d’un espace de noms, consultez [création de hiérarchies dans WMI](creating-hierarchies-within-wmi.md).

Les classes de pilote peuvent parfois être « bloquées » si le chargement du pilote est interrompu ou si d’autres opérations anormales se produisent. Le fournisseur WDM recherche et nettoie uniquement les classes « bloquées » lors de l’installation d’un nouveau pilote ou lorsque la valeur de clé de Registre **WDMProvider du logiciel \\ Microsoft \\ WBEM \\** **ProcessStrandedClasses** est définie sur **true**. La définition de cette valeur sur **true** ralentit les performances de démarrage de WMI en raison de l’opération de nettoyage. La valeur par défaut est **FALSE**. Le fournisseur WDM vérifie cette valeur de Registre uniquement lorsque l' \\ espace de noms WMI racine est ouvert pour la première fois.

Si des modifications de sécurité sont apportées à un pilote de périphérique WDM, les modifications n’entrent pas en vigueur tant que le fournisseur WDM n’est pas chargé et rechargé. pour ce faire, vous devez arrêter et redémarrer le service de gestion de Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de WMI](using-wmi.md)
</dt> </dl>

 

 
