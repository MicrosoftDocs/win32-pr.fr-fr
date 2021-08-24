---
description: Étant donné qu’une action personnalisée peut être planifiée dans les tables d’interface utilisateur et d’exécution, et qu’elle peut être exécutée dans le processus du service ou du client, une action personnalisée peut potentiellement s’exécuter plusieurs fois.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Options de planification de l’exécution des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91adbee99684a5a9db0701c2371c8c517547b4d91881518d72fe7c25c0d189be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520099"
---
# <a name="custom-action-execution-scheduling-options"></a>Options de planification de l’exécution des actions personnalisées

Étant donné qu’une action personnalisée peut être planifiée dans les tables d’interface utilisateur et d’exécution, et qu’elle peut être exécutée dans le processus du service ou du client, une action personnalisée peut potentiellement s’exécuter plusieurs fois.

Notez que le programme d’installation :

-   Exécute des actions dans une table de séquences immédiatement par défaut.
-   N’exécute pas d’action si le champ expression conditionnelle de la table Sequence prend la valeur false.
-   Traite la table de séquence d’interface utilisateur dans le processus client si le niveau d’interface de l’utilisateur interne est défini sur le mode d’interface utilisateur complet (consultez [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) pour obtenir une description des niveaux de l’interface utilisateur).
-   est un service enregistré par défaut lors de l’utilisation de Windows 2000 et, dans ce cas, la table d’exécution des séquences est traitée dans le service d’installation.

Vous pouvez utiliser les indicateurs d’option suivants pour contrôler plusieurs exécutions immédiates d’actions personnalisées. Pour définir une option, ajoutez la valeur de ce tableau à la valeur du champ type de la [table CustomAction](customaction-table.md). Aucun des indicateurs suivants ne doit être utilisé avec des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md).

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>valeurs
</dt> <dd>

Hexadécimal : 0x00000000

Décimal : 0

Exécutez toujours. L’action peut s’exécuter deux fois si elle est présente dans les deux tables de séquence.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Hexadécimal : 0x00000100

Décimal : 256

Ne pas exécuter plus d’une fois si elle est présente dans les deux tables de séquence. Ignore toujours l’action dans la séquence d’exécution si la séquence d’interface utilisateur a été exécutée. Aucun effet dans la séquence d’interface utilisateur. L’action ne doit pas obligatoirement être présente ou exécutée dans la séquence d’interface utilisateur pour être ignorée dans la séquence d’exécution. Non affecté par l’inscription du service d’installation.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Hexadécimal : 0x00000200

Décimal : 512

Exécuter une fois par processus si les deux tables de séquences. Ignore l’action dans la séquence d’exécution si la séquence d’interface utilisateur a été exécutée dans le même processus, par exemple s’exécuter dans le processus client. Permet d’empêcher les actions qui modifient l’état de la session, telles que les données de la propriété et de la base de données, de s’exécuter deux fois.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Hexadécimal : 0x00000300

Décimal : 768

S’exécute uniquement en cas d’exécution sur le client après l’exécution de la séquence d’interface utilisateur. L’action s’exécute uniquement si la séquence d’exécution est exécutée sur le client suivant la séquence d’interface utilisateur. Peut être utilisé pour fournir une logique/ou logique, ou pour supprimer le traitement lié à l’interface utilisateur s’il est déjà fait pour la session cliente.

</dd> </dl>

Notez que pour exécuter une action personnalisée pendant deux modes d’exécution différents, créez deux entrées dans la [table CustomAction](customaction-table.md) . Par exemple, pour avoir une action personnalisée qui appelle une bibliothèque de liens dynamiques (DLL) C/C++ ( [type d’action personnalisée 1](custom-action-type-1.md)) quand le mode est MSIRUNMODE \_ planifié et MSIRUNMODE \_ Rollback, placez deux entrées dans la table CustomAction qui appellent la même dll mais qui ont des types numériques différents. Incluez le code qui appelle [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) pour déterminer quand exécuter l’action personnalisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence des actions personnalisées](custom-action-reference.md)
</dt> <dt>

[À propos des actions personnalisées](about-custom-actions.md)
</dt> <dt>

[Utilisation d’actions personnalisées](using-custom-actions.md)
</dt> </dl>

 

 



