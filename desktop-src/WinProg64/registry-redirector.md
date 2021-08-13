---
title: Redirecteur du Registre
description: Le redirecteur du Registre isole les applications 32 bits et 64 bits en fournissant des vues logiques distinctes de certaines parties du Registre sur WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- guide de programmation Windows 64 bits 64-bits Windows programmation, redirecteur de registre
- redirecteur du registre 64-bit Windows programmation
- redirection de la programmation Windows bits 64
- WOW64 64-bit Windows programmation, redirecteur de registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac810a6ce2dba049f7b7e5b9d28386cda89712f2833eb7bf4f7892df59b34ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561505"
---
# <a name="registry-redirector"></a>Redirecteur du Registre

Le redirecteur du Registre isole les applications 32 bits et 64 bits en fournissant des vues logiques distinctes de certaines parties du Registre sur WOW64. Le redirecteur du Registre intercepte les appels de Registre 32 bits et 64 bits vers leurs vues de Registre logique respectives et les mappe à l’emplacement de registre physique correspondant. Le processus de redirection est transparent pour l’application. par conséquent, une application 32 bits peut accéder aux données du registre comme si elles étaient exécutées sur 32 bits Windows même si les données sont stockées dans un emplacement différent sur 64 bits Windows.

**Windows 10 sur ARM :** en plus de la vue logique 32 bits pour les applications x86, Windows 10 sur ARM comprend une vue logique distincte pour les applications ARM 32 bits.

Un sous-ensemble de clés sous les chemins de Registre redirigés est partagé. les appels de Registre 32 bits aux clés partagées ne sont pas redirigés. Au lieu de cela, une copie physique de la clé est mappée à chaque vue logique du Registre. Pour obtenir la liste des clés redirigées et des clés partagées, consultez [clés de Registre affectées par WOW64](shared-registry-keys.md).

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** Pour permettre l’interopérabilité des applications par le biais de COM et d’autres mécanismes, un sous-ensemble de clés de Registre redirigées est également *reflété*. Le processus de réflexion du Registre copie les clés de Registre et les valeurs entre deux vues du Registre pour les maintenir synchronisées. la réflexion du registre a été supprimée à partir de Windows 7 et Windows Server 2008 R2. Pour plus d’informations, consultez [Registry Reflection](registry-reflection.md).

Le scénario suivant illustre l’utilisation de ces vues logiques :

-   Une application x86 32 bits vérifie l’existence de la clé de Registre suivante : **HKEY \_ local \_ machine \\ Software \\ Hello**. Si la clé n’existe pas, l’application la crée avec la valeur par défaut « Hello 32-bit x86 World ». dans le cas contraire, il lit et affiche la valeur.
-   La même application est modifiée pour écrire « Hello 64-bit World » au lieu de « Hello 32-bit x86 World » et recompilée en tant qu’application ARM64 ou x64 64 bits.
-   **Windows 10 sur ARM :** La même application est modifiée pour écrire « Hello 32-bit ARM World » et être recompilée comme une application ARM 32 bits.
-   lorsque l’application x86 32 bits est exécutée sur le Windows 64 bits, elle affiche « Hello 32-bit x86 world ». Lorsque l’application 64 bits est exécutée, elle affiche « Hello 64-bit World ». **Windows 10 sur ARM :** lorsque l’application arm 32 bits est exécutée sur le Windows ARM64 64 bits, elle affiche « Hello 32-bit arm world ». Toutes les applications appellent les mêmes fonctions de Registre avec le même handle prédéfini et le même nom de clé ; la différence est que chaque application fonctionne sur sa vue logique du Registre, et chaque vue est mappée à un emplacement physique distinct du Registre, ce qui permet de conserver toutes les versions de la chaîne intactes.

Les clés redirigées sont mappées aux emplacements physiques sous **Wow6432Node**. Par exemple, **HKEY \_ local \_ machine \\ Software** est redirigé vers **HKEY \_ local \_ machine \\ Software \\ Wow6432Node**. Toutefois, l’emplacement physique des clés redirigées doit être considéré comme réservé par le système. Les applications ne doivent pas accéder directement à l’emplacement physique d’une clé, car cet emplacement peut changer. Pour plus d’informations, consultez [accès à une autre vue de Registre](accessing-an-alternate-registry-view.md).

**Windows 10 sur ARM :** Les clés redirigées ARM 32 bits sont mappées aux emplacements physiques sous WowAA32Node.

Pour aider les applications 32 bits qui écrivent les données **reg \_ SZ** ou **reg développer les données \_ \_ SZ** contenant% ProgramFiles% ou% COMMONPROGRAMFILES% dans le registre, WOW64 intercepte ces opérations d’écriture et les remplace par « % ProgramFiles (x86)% » et « % COMMONPROGRAMFILES (x86)% ». Par exemple, si le répertoire Program Files se trouve sur le lecteur C, « % ProgramFiles (x86)% » se développe en « C : \\ Program Files (x86) ». Le remplacement se produit uniquement si les conditions suivantes sont remplies :

-   La chaîne doit commencer par% ProgramFiles% ou% CommonProgramFiles%. Si la chaîne commence par un espace ou un caractère autre que%, elle n’est pas remplacée.
-   Le cas de% ProgramFiles% ou% COMMONPROGRAMFILES% doit être exactement tel qu’indiqué, car la comparaison de chaînes respecte la casse. Par exemple, si la chaîne commence par% CommonProgramFiles% au lieu de% COMMONPROGRAMFILES%, elle n’est pas remplacée.
-   La chaîne ne peut pas dépasser le \_ chemin d’accès maximal \* 2 + 15 caractères. Si elle dépasse cette longueur, elle n’est pas remplacée.
-   Impossible d’ouvrir la clé avec la clé \_ WOW64 \_ 64KEY. Cet indicateur spécifie que les opérations sur la clé doivent être exécutées sur la vue de Registre 64 bits, de sorte qu’elles ne sont pas remplacées. Pour plus d’informations, consultez [accès à une autre vue de Registre](accessing-an-alternate-registry-view.md).

**Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** L' \_ \_ \_ indicateur 64KEY de clé wow 64 n’a aucune incidence sur la nécessité ou non de remplacer une clé. cet indicateur affecte le remplacement à partir de Windows 7 et Windows Server 2008 R2.

En outre, les \_ clés de Reg SZ ou reg \_ expand \_ qui contiennent system32 sont remplacées par SysWOW64. La chaîne doit commencer par le chemin d’accès pointant vers ou sous% windir% \\ system32. La comparaison de chaînes n’est pas sensible à la casse. Les variables d’environnement sont développées avant de correspondre au chemin d’accès, de sorte que tous les chemins d’accès suivants sont remplacés :% windir% \\ system32,% systemroot% \\ system32 et C : \\ Windows \\ system32. ce correctif s’applique uniquement aux clés qui ont été reflétées avant Windows 7.

Pour plus d'informations, voir les rubriques suivantes :

-   [Réflexion du Registre](registry-reflection.md)
-   [Clés de Registre affectées par WOW64](shared-registry-keys.md)
-   [Accès à une autre vue de Registre](accessing-an-alternate-registry-view.md)
-   [Exemple de redirection du Registre sur WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Accès au registre à distance en Windows 64 bits](remote-registry-access-in-64-bit-windows.md)

 

 




