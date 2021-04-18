---
title: Accès à une autre vue de Registre
description: Par défaut, une application 32 bits s'exécutant sur WOW64 accède à la vue de Registre 32 bits et une application 64 bits accède à la vue de Registre 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- affichages du registre de la programmation Windows 64 bits
- WOW64, programmation Windows 64 bits, affichages du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "106536223"
---
# <a name="accessing-an-alternate-registry-view"></a>Accès à une autre vue de Registre

Par défaut, une application 32 bits s'exécutant sur WOW64 accède à la vue de Registre 32 bits et une application 64 bits accède à la vue de Registre 64 bits. Les indicateurs suivants permettent aux applications 32 bits d’accéder aux clés redirigées dans la vue de Registre 64 bits et aux applications 64 bits d’accéder aux clés redirigées dans l’affichage du Registre 32 bits. Ces indicateurs n’ont aucun effet sur les clés de Registre partagées. Pour plus d’informations, consultez [clés de Registre affectées par WOW64](shared-registry-keys.md).



| Nom de l’indicateur         | Valeur  | Description                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLÉ \_ WOW64 \_ 64KEY | 0x0100 | Accédez à une clé 64 bits à partir d’une application 32 bits ou 64 bits.                                                                                                                                                                                   |
| CLÉ \_ WOW64 \_ 32KEY | 0x0200 | Accédez à une clé 32 bits à partir d’une application 32 bits ou 64 bits.<br/>**Windows 10 sur ARM :** Cela fait référence à la vue de Registre ARM 32 bits pour les processus ARM 32 bits et à la vue de Registre x86 32 bits pour les processus ARM64 32 et 64 bits. |



 

Ces indicateurs peuvent être spécifiés dans le paramètre *samDesired* des fonctions de Registre suivantes :

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

Vous \_ pouvez spécifier la clé WOW64 \_ 32KEY ou la clé \_ WOW64 \_ 64KEY. Si les deux indicateurs sont spécifiés, la fonction échoue avec un paramètre d’erreur \_ non valide \_ .

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Si les deux indicateurs sont spécifiés, le comportement s de la fonction n’est pas défini.

La fonction [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) ne peut pas être utilisée pour accéder à une autre vue de registre.

Voici les meilleures pratiques pour accéder au registre à partir d’une application :

-   Une fois que l’application a accédé à une autre vue du Registre à l’aide de l’un des indicateurs, toutes les opérations suivantes (créer, supprimer ou ouvrir) sur les clés de Registre enfants doivent utiliser le même indicateur de manière explicite. Dans le cas contraire, il peut y avoir un comportement inattendu.
-   Pour énumérer avec précision toutes les clés dans les deux vues, effectuez l’énumération en deux étapes. La première passe doit utiliser un handle ouvert avec l’un des indicateurs, et l’autre passe doit utiliser un handle ouvert avec l’autre indicateur.

> [!Note]  
> Les clés **Wow6432Node** et **WowAA32Node** sont réservées. Pour des fins de compatibilité, les applications ne doivent pas utiliser ces clés directement.

 

Pour plus d’informations sur l’accès à l’affichage de registre de remplacement par le biais de WMI, consultez [demande de données WMI sur une plateforme 64 bits](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Redirecteur du Registre](registry-redirector.md)
</dt> <dt>

[Réflexion du Registre](registry-reflection.md)
</dt> </dl>

 

