---
description: Pour l’utilisateur, le système semble être activé ou désactivé.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: États d’alimentation du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efde8a130d6dbe2b44c34e8ab45b973a64f3b255
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120814"
---
# <a name="system-power-states"></a>États d’alimentation du système

Pour l’utilisateur, le système semble être activé ou désactivé. Il n’existe aucun autre État détectable. Toutefois, le système prend en charge plusieurs États d’alimentation qui correspondent aux États d’alimentation définis dans la spécification ACPI (Advanced Configuration and Power Interface). Il existe également des variantes de ces États, comme la veille hybride et le démarrage rapide. Cette rubrique présente ces États et décrit la façon dont ils sont liés les uns aux autres.

> [!NOTE]
> Les intégrateurs système et les développeurs qui créent des pilotes ou des applications avec un service système doivent être particulièrement attentifs aux problèmes de qualité des pilotes, tels que les fuites de mémoire. Bien que la qualité du pilote ait toujours été importante, le temps de mise en route entre les redémarrages du noyau peut être beaucoup plus long que sur les versions précédentes du système d’exploitation, car les arrêts et les arrêts initiés par l’utilisateur sont conservés, le noyau, les pilotes et les services sont conservés et restaurés, et non redémarrés.

 

Le tableau suivant répertorie les États d’alimentation ACPI du plus élevé au plus faible consommation d’énergie.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>État d’alimentation</th>
<th>État ACPI</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>fonctionne<br/></td>
<td>S0<br/></td>
<td>Le système est entièrement utilisable. Les composants matériels qui ne sont pas en cours d’utilisation peuvent économiser de l’énergie en entrant un état d’alimentation inférieur.<br/></td>
</tr>
<tr class="even">
<td>Veille<br/> (Veille moderne)<br/></td>
<td>S0 faible consommation d’énergie<br/></td>
<td>Certains systèmes SoC prennent en charge un état de faible consommation d’énergie, connu sous le nom de <a href="/windows-hardware/design/device-experiences/modern-standby">mise en veille moderne</a>. Dans cet État, le système peut très rapidement passer de l’État faible consommation à l’État haute consommation, afin qu’il puisse répondre rapidement aux événements matériels et réseau. Les systèmes qui prennent en charge la mise en veille moderne n’utilisent pas S1-S3.<br/></td>
</tr>
<tr class="odd">
<td>Veille<br/></td>
<td>S1<br/> S2<br/> S3<br/></td>
<td>Le système semble être désactivé. La puissance consommée dans ces États (S1-S3) est inférieure à S0 et supérieure à S4 ; S3 consomme moins d’énergie que S2 et S2 consomme moins d’énergie que S1. Les systèmes prennent généralement en charge l’un de ces trois États, pas les trois.<br/> Dans ces États (S1-S3), la mémoire volatile est actualisée pour maintenir l’état du système. Certains composants restent sous tension, de sorte que l’ordinateur peut sortir de veille de l’entrée à partir du clavier, du réseau local ou d’un périphérique USB.<br/> La <em>veille hybride</em>, utilisée sur les postes de travail, est l’endroit où un système utilise un fichier de mise en veille prolongée avec S1-S3. Le fichier de mise en veille prolongée enregistre l’état du système dans le cas où le système perd de l’électricité en veille.<br/>
<blockquote>
[!Note]<br />
Les systèmes SoC qui prennent en charge la mise en veille moderne (état de faible consommation d’énergie) n’utilisent pas S1-S3.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Mise en veille prolongée<br/></td>
<td>S4<br/></td>
<td>Le système semble être désactivé. La consommation d’énergie est réduite au niveau le plus bas. Le système enregistre le contenu de la mémoire volatile dans un fichier de mise en veille prolongée pour conserver l’état du système. Certains composants restent sous tension, de sorte que l’ordinateur peut sortir de veille de l’entrée à partir du clavier, du réseau local ou d’un périphérique USB. Le contexte de travail peut être restauré s’il est stocké sur un support non volatile. <br/> Le <em>démarrage rapide</em> est l’endroit où l’utilisateur est déconnecté avant la création du fichier de mise en veille prolongée. Cela permet un plus petit fichier de mise en veille prolongée, mieux adapté aux systèmes avec des capacités de stockage moins importantes.<br/></td>
</tr>
<tr class="odd">
<td>Désactivé<br/></td>
<td>S5<br/></td>
<td>Le système semble être désactivé. Cet État est constitué d’un arrêt complet et d’un cycle de démarrage.<br/></td>
</tr>
<tr class="even">
<td>Mécanique désactivé<br/></td>
<td>G3<br/></td>
<td>Le système est complètement éteint et n’utilise pas de puissance. Le système revient à l’état de travail uniquement après un redémarrage complet.<br/></td>
</tr>
</tbody>
</table>



 

L’énumération de l' [**\_ \_ État d’alimentation du système**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) définit les valeurs utilisées pour spécifier les États d’alimentation du système.

## <a name="working-state-s0"></a>État de travail (S0)

Dans le cadre de l’état de travail, le système est en éveil et en cours d’exécution. En termes simples, l’appareil est « activé ». Que l’écran soit activé ou désactivé, l’appareil est en état d’exécution complet. Pour économiser de l’énergie, en particulier sur les appareils fonctionnant sur batterie, nous vous recommandons vivement de mettre hors tension les composants matériels lorsqu’ils ne sont pas utilisés.

> [!IMPORTANT]
> Mettez hors tension les composants matériels chaque fois qu’ils ne sont pas utilisés, quel que soit l’État. Une faible consommation d’énergie est un point important à prendre en compte pour les consommateurs de périphériques mobiles.

 

## <a name="sleep-state-modern-standby"></a>État de veille (veille moderne)

En mode faible consommation S0 de l’état de fonctionnement, également appelé [veille moderne](/windows-hardware/design/device-experiences/modern-standby), le système continue à fonctionner partiellement. Pendant la mise en veille moderne, le système peut rester à jour chaque fois qu’un réseau approprié est disponible et se réveiller quand une action en temps réel est requise, telle que la maintenance du système d’exploitation. Les réveils de secours modernes sont beaucoup plus rapides que S1-S3. Pour plus d’informations, consultez la page [mise en veille moderne](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> La mise en veille moderne est disponible uniquement sur certains systèmes SoC. Lorsqu’il est pris en charge, le système ne prend pas en charge S1-S3.

 

## <a name="sleep-state-s1-s3"></a>État de veille (S1-S3)

Le système entre en mode veille en fonction d’un certain nombre de critères, y compris l’activité de l’utilisateur ou de l’application, ainsi que les préférences définies par l’utilisateur sur la page de **veille Power &** de l’application **paramètres** . Par défaut, le système utilise l’état de veille de niveau inférieur pris en charge par tous les appareils de mise en éveil activés. Pour plus d’informations sur la façon dont le système détermine le moment où la mise en veille doit être entrée, consultez [critères de veille du système](system-sleep-criteria.md).

Avant que le système n’entre en veille, il détermine l’état de veille approprié, avertit les applications et les pilotes de la transition en attente, puis fait passer le système à l’état de veille. Dans le cas d’une transition critique, par exemple lorsque le seuil de batterie critique est atteint, le système ne notifie pas les applications et les pilotes. Les applications doivent être préparées pour cela et prendre les mesures appropriées lorsque le système revient à l’état de travail.

Dans ces États (S1-S3), la mémoire volatile est actualisée pour maintenir l’état du système. Certains composants restent sous tension, de sorte que l’ordinateur peut sortir de veille de l’entrée à partir du clavier, du réseau local ou d’un périphérique USB.

Le système sort également du mode veille en réponse à l’activité de l’utilisateur ou à un événement de mise en éveil défini par une application. Pour plus d’informations, consultez [événements de mise en éveil du système](system-wake-up-events.md). Le temps nécessaire au système pour sortir de veille dépend de l’état de veille à partir duquel il sort. Le système met plus de temps à sortir de veille d’un état de faible consommation (S3) qu’à partir d’un État plus élevé (S1) en raison du travail supplémentaire que le matériel peut avoir à faire (stabiliser l’alimentation, réinitialiser le processeur, etc.).

> [!Caution]  
> Lors de l’appel de [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate), la valeur **\_ \_ requise de mode absence es** doit être utilisée uniquement lorsque cela est absolument nécessaire par les applications multimédias qui requièrent que le système exécute des tâches en arrière-plan, telles que l’enregistrement de contenu de télévision ou la diffusion de médias sur d’autres appareils pendant que le système semble être en veille. Les applications qui ne nécessitent pas de traitement en arrière-plan critique ou qui s’exécutent sur des ordinateurs portables ne doivent pas activer le mode away, car elles empêchent le système d’économiser de l’énergie en entrant une véritable mise en veille.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Veille hybride (S1-S3 + fichier de mise en veille prolongée)

La mise en *veille hybride* est un état spécial qui est une combinaison des États de veille et de veille prolongée, c’est lorsqu’un système utilise un fichier de mise en veille prolongée avec S1-S3. Elle n’est disponible que sur certains systèmes. Lorsqu’il est activé, le système écrit un fichier de mise en veille prolongée, mais utilise un état de veille avec une meilleure alimentation. En cas de perte d’alimentation alors que le système est en veille, le système sort de la veille prolongée, ce qui prend plus de temps mais restaure l’état du système de l’utilisateur.

## <a name="hibernate-state-s4"></a>État de mise en veille prolongée (S4)

Windows utilise la veille prolongée pour offrir une expérience de démarrage rapide. Lorsqu’il est disponible, il est également utilisé sur les appareils mobiles pour étendre la durée de vie de la batterie utilisable d’un système en fournissant un mécanisme permettant d’enregistrer l’ensemble de l’état utilisateur avant d’arrêter le système. Dans une transition de mise en veille prolongée, tout le contenu de la mémoire est écrit dans un fichier sur le lecteur système principal, le *fichier de mise en veille prolongée*. Cela préserve l’état du système d’exploitation, des applications et des périphériques. Dans le cas où l’empreinte mémoire combinée consomme toute la mémoire physique, le fichier de mise en veille prolongée doit être suffisamment grand pour garantir l’espace nécessaire à l’enregistrement de tout le contenu de la mémoire physique. Étant donné que les données sont écrites dans un stockage non volatile, la DRAM n’a pas besoin de conserver une auto-actualisation et peut être mise hors tension, ce qui signifie que la consommation électrique de la mise en veille prolongée est très faible, presque identique à la mise hors tension.

Pendant un arrêt et un démarrage complets (S5), toute la session utilisateur est détruite et redémarrée au démarrage suivant. En revanche, pendant une mise en veille prolongée (S4), la session utilisateur est fermée et l’état utilisateur est enregistré.

### <a name="fast-startup-reduced-hibernation-file"></a>Démarrage rapide (fichier de mise en veille prolongée réduit)

Le *démarrage rapide* est un type d’arrêt qui utilise un fichier de mise en veille prolongée pour accélérer le démarrage suivant. Pendant ce type d’arrêt, l’utilisateur est déconnecté avant la création du fichier de mise en veille prolongée. Le démarrage rapide permet un plus petit fichier de mise en veille prolongée, mieux adapté aux systèmes avec des capacités de stockage moindres. Pour plus d’informations, consultez [types de fichiers de mise en veille prolongée](#hibernation-file-types).

Lors de l’utilisation du démarrage rapide, le système apparaît à l’utilisateur comme s’il s’agissait d’un arrêt complet (S5), même si le système est en train de passer par S4. Cela comprend la manière dont le système répond aux alarmes de sortie de l’appareil.

Le démarrage rapide déconnecte les sessions utilisateur, mais le contenu du noyau (session 0) est écrit sur le disque dur. Cela permet un démarrage plus rapide.

Pour lancer par programmation un arrêt rapide de style de démarrage, appelez la fonction [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) avec l’indicateur d' **arrêt \_ hybride** ou la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) avec l’indicateur d' **\_ \_ arrêt EWX hybride** .

> [!Note]  
> À compter de Windows 8, le démarrage rapide est la transition par défaut lorsqu’un arrêt système est demandé. Un arrêt complet (S5) se produit lorsqu’un redémarrage du système est demandé (ou lorsqu’une application appelle une API d’arrêt).

 

### <a name="entering-hibernation"></a>Entrée en veille prolongée

Quand une demande de mise en veille prolongée est effectuée, les étapes suivantes se produisent lorsque le système entre en veille prolongée :

1.  Les applications et les services sont avertis
2.  Les pilotes sont avertis
3.  L’état utilisateur et système est enregistré sur le disque dans un format compressé
4.  Le microprogramme est averti

> [!Note]  
> À partir de Windows 8, tous les cœurs du système sont utilisés pour compresser les données en mémoire et les écrire sur le disque.

 

Pour lancer par programmation une transition de mise en veille prolongée, appelez la fonction [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

### <a name="resuming-from-hibernation"></a>Reprise de la mise en veille prolongée

Lorsqu’un système sort de la mise en veille prolongée.

Lorsqu’un système est sous tension, les étapes suivantes se produisent lorsque le système quitte la mise en veille prolongée.

1.  PUBLICATION système
2.  La mémoire système est décompressée et restaurée à partir du fichier de mise en veille prolongée
3.  Initialisation de l’appareil
4.  Les pilotes sont restaurés à l’État dans lequel ils se trouvaient avant la mise en veille prolongée
5.  Les services sont restaurés à l’État dans lequel ils se trouvaient avant la mise en veille prolongée
6.  Le système devient disponible pour la connexion

Une reprise à partir de la mise en veille prolongée commence par une publication système similaire à un arrêt de S5. Le gestionnaire de démarrage du système d’exploitation détermine qu’une reprise de la mise en veille prolongée est nécessaire en détectant un fichier de mise en veille prolongée valide. Ensuite, il indique au système de reprendre, de restaurer le contenu de la mémoire et tous les registres architecturaux. Dans le cas d’une reprise à partir de la mise en veille prolongée, le contenu de la mémoire système est lu à partir du disque, décompressé et restauré, plaçant le système dans l’état exact dans lequel il se trouvait lors de sa mise en veille prolongée. Une fois la mémoire restaurée, les appareils sont redémarrés, l’ordinateur revient à l’État en cours d’exécution et est prêt pour la connexion.

> [!Note]  
> Lors de la reprise de la mise en veille prolongée, les pilotes et les services sont avertis, mais ils ne sont pas redémarrés. Ils sont restaurés uniquement à l’État dans lequel ils se trouvaient avant la mise en veille prolongée.

 

### <a name="hibernation-file-types"></a>Types de fichiers de mise en veille prolongée

Les fichiers de mise en veille prolongée sont utilisés pour la veille hybride, le démarrage rapide et la mise en veille standard (décrite plus haut). Il existe deux types, différenciés par la taille, un fichier de mise en veille prolongée et de taille réduite. Seul le démarrage rapide peut utiliser un fichier de mise en veille prolongée réduit.



| Type de fichier de mise en veille prolongée | Taille par défaut           | Prend en charge...                           |
|-----------------------|------------------------|---------------------------------------|
| Complète                  | 40% de la mémoire physique | mise en veille prolongée, veille hybride, démarrage rapide |
| Baisse               | 20% de la mémoire physique | démarrage rapide                          |



 

Pour vérifier ou modifier le type de fichier de mise en veille prolongée utilisé, exécutez l’utilitaire **powercfg.exe** . Les exemples suivants montrent comment procéder. Pour plus d’informations, exécuter `powercfg /? hibernate`.



| Exemple                                                                        | Description                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | **Vérifiez le type de fichier de mise en veille prolongée.** Lorsqu’un fichier de mise en veille prolongée est utilisé, l’état des résultats indique que la mise en veille prolongée est une option disponible. Lorsqu’un fichier de mise en veille prolongée est utilisé, les résultats indiquent que la mise en veille prolongée n’est pas prise en charge. Si le système n’a aucun fichier de mise en veille prolongée, les résultats indiquent que la mise en veille prolongée n’a pas été activée.<br/> |
| `powercfg /h /type full`<br/>                                     | **Définissez le type de fichier de mise en veille prolongée sur Full.** Cela n’est pas recommandé sur les systèmes avec moins de 32 Go de stockage.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Modifiez le type de fichier de mise en veille prolongée en le réduisant.** Si la commande retourne « le paramètre est incorrect », consultez l’exemple suivant.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Réessayez de modifier le type de fichier de mise en veille prolongée pour le réduire.** Si le fichier de mise en veille prolongée est défini sur une taille personnalisée supérieure à 40%, vous devez d’abord définir la taille du fichier sur zéro. Réessayez ensuite la configuration réduite.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>État de désactivation (S5)

L’état de désactivation est lorsque le système s’arrête complètement sans un fichier de mise en veille prolongée. La désactivation douce est également appelée « arrêt complet ». Pendant un arrêt et un démarrage complets, toute la session utilisateur est détruite et redémarrée au démarrage suivant. Par conséquent, un démarrage/démarrage à partir de cet État prend beaucoup plus de temps que S1-S4. Un arrêt complet (S5) se produit lorsqu’un redémarrage du système est demandé (ou lorsqu’une application appelle une API d’arrêt).

## <a name="mechanical-off-state-g3"></a>État de désactivation mécanique (G3)

Dans cet État, le système est complètement éteint et n’utilise pas de puissance. Le système revient à l’état de travail uniquement après un redémarrage complet.

## <a name="wake-on-lan-behavior"></a>Comportement Wake-on-LAN

La fonction Wake-on-LAN (WOL) sort l’ordinateur de l’état d’alimentation faible lorsqu’une carte réseau détecte un événement WOL (en général, un paquet Ethernet spécialement construit).

WOL est pris en charge à partir du mode veille (S3) ou veille prolongée (S4). Il n’est pas pris en charge pour les États d’arrêt de démarrage rapide ou de désactivation douce (S5). Les cartes réseau ne sont pas armées pour la sortie de veille dans ces États, car les utilisateurs ne s’attendent pas à ce que leurs systèmes se réveillent eux-mêmes.

> [!Note]  
> WOL n’est pas officiellement pris en charge par la désactivation logicielle (S5). Toutefois, le BIOS sur certains systèmes peut prendre en charge les cartes réseau mettant pour la mise en éveil, même si Windows n’est pas impliqué dans le processus.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> </dl>
