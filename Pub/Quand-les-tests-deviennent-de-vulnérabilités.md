![Test](https://images.pexels.com/photos/459793/pexels-photo-459793.jpeg?w=1260&h=750&auto=compress&cs=tinysrgb)

# FRANCAIS :fr:

[English version](https://github.com/SwitHak/SwitHak.github.io/blob/master/Pub/Quand-les-tests-deviennent-de-vuln%C3%A9rabilit%C3%A9s.md#english-us)
## Quand les tests deviennent des vulnérabilités

### Une bonne intention...
Tester les applications, les mises à jour est plus que jamais nécessaire, et les dernières attaques sur la supply chain en ont bien rappelé les enjeux.
Tester une application ou une mise à jour est un travail plutôt redondant, beaucoup d'automatisation est alors déployée afin de réduire au maximum les interactions utilisateurs avec l'environnement de test.
Afin de bien mener ces derniers, un environnement de test est alors configuré. il est généralement basé sur le master de l'entreprise et contient des configurations spécifiques à l'entreprise. 
Il a des lecteurs réseaux connectés aux dossiers contenant les fichiers exécutables mis au banc d'essai, etc.
Ces environnements ne sont pas créés pour durer dans le temps et les mesures de sécurité qui leur sont appliquées sont très (trop) souvent légères quand elles ne sont pas inexistantes.

### ...qui peut révéler beaucoup d'Information...
Les environnements de tests sont du pain béni pour la collecte d'information quand ils ne sont pas sécurisés correctement. Bien souvent, ils ne sont pas connus des équipes de sécurité, et par extension, ne sont pas soumis aux pratiques de sécurité générales ou celles-ci sont volontairement occultées.
Ces mines peuvent révéler des informations utiles pour une future attaque:
- Versions des logiciels utilisés
- Identifiants et mots de passe
- Jeux de données de test [même si l'anonymisation des données devrait devenir plus générale](http://www.comptoirsecu.fr/podcast/%C3%A9pisode-46-protection-des-donn%C3%A9es-personnelles/)
- Accès au réseau interne de l'entreprise
- ...

### ...quand elle ne devient pas la porte d'entrée d'attaques !
Mal configurés et exposés, le cocktail est bien souvent explosif. Les environnements de test par leur faible (absence) de sécurité peuvent devenir les points d'entrée d'attaque contre un système d'information. 
Il est en effet facile d'entrer sur une machine exposée et de l'utiliser en pivot pour accéder au réeau interne. 
Grâce aux informations trouvées sur ces environnements, les attaquants peuvent mieux appréhender et orienter leurs actions afin de les rendre plus pertinentes et, par extension, possiblement plus dommageables.


### Les bonnes pratiques pour tous !
Il n'y a pas de recette universelle sur comment bien configurer un environnement de test, mais voici quelques pistes pour éviter que vos tests virent au cauchemar.
- Si la nécessité de connecter à Internet et au réseau Interne tu n'as point, tu ne le feras pas !
- Prévenir les services de sécurité informatique de l'entreprise, tu feras !
- Les jeux de tests, tu anonymiseras (si possible) !
- Les mises à jour de ces systèmes, tu n'oublieras pas !
- Les .txt avec les mots de passe en clair sur le bureau, tu ne feras pas !
- Les machines, une fois les tests terminés, tu supprimeras !

D'autres conseils existent, le plus important reste qu'il ne faut pas que des machines de tests oubliées deviennent le point d'entrée d'attaque par la négligence d'une personne.

# English :us:

## When tests become vulnerabilities

#### A good intention...
Testing applications, updates is more necessary than ever, and the latest attacks on the supply chain have reminded us of the stakes involved.
Testing an application or an update is a fairly redundant job, so a lot of automation is deployed to minimize user interaction with the test environment.
In order to carry out these tests, a test environment is then configured. It is generally based on the enterprise master and contains enterprise-specific configurations. 
It has network drives connected to folders containing the executable files put to the test bed, etc.
These environments are not created to last over time and the security measures applied to them are very (too) often light when they are not non-existent.

##### .... that can reveal a lot of Information... 
Test environments are blessed bread for collecting information when they are not secured properly. They are often not known to security teams, and by extension, are not subject to general security practices or are intentionally concealed.
These mines may reveal information useful for a future attack:
- Software versions used
- Identifiers and passwords
- Test datasets [although anonymization of data should become more general](http://www.comptoirsecu.fr/podcast/%C3%A9pisode-46-protection-des-donn%C3%A9es-personnelles/)
- Access to the company's internal network
- ...

#### ...when it doesn't become the gateway to attack!
Poorly configured and exposed, the cocktail is often explosive. Test environments because of their weak (absence) security can become the entry points for attacking an information system. 
It is easy to enter an exposed machine and use it as a pivot to access the internal reef. 
Thanks to the information found on these environments, attackers can better apprehend and direct their actions to make them more relevant and, by extension, potentially more damaging.


#### Good practices for all!
There is no universal recipe on how to configure a test environment properly, but here are a few hints to prevent your tests from turning into a nightmare.
- If you don't have the need to connect to the Internet and the internal network, you won't do it!
- Notify the company's IT security services, you will do it!
- Test samples, you will anonymize (if possible)
- Upgrades to these systems, you won't forget!
- The. txt with clear passwords on the desktop, you will don't!
- The machines, once the tests are finished, you will delete!

Other tips exist, the most important thing is that forgotten test machines should not become the entry point of attack by someone's negligence.

SwitHak
